# Random Forest Models
Random Forest Models of Fast MTT Decision and Motion Estimation for Inter Coding of H.266/VVC

This is the official repository of models for the paper "Fast MTT Decision and Motion Estimation for Inter Coding of H.266/VVC," submitted to IEEE Access on XXX. XX, 2020, and now in press. See the link ()

Executable Files --> "Model_BT.xml" and "Model_HV.xml"

https://github.com/karta28533/Random-Forest-Models/blob/main/Random%20Forest%20Models.rar

Model_BT.xml is a model for BT/TT

Model_HV.xml is a model for Hor/Ver

We uploaded executable files with encoding configurations and batch files containing parameters to result in tables of submitted paper. Note that executable files (.exe files) have been compiled using VS 2019 on Windows 10. The base software is VTM 3.0 (official site to download is as follows. https://vcgit.hhi.fraunhofer.de/jvet/VVCSoftware_VTM/-/tree/VTM-3.0)

The following link is OpenCV 3.2.0 version, please download and install it into the VTM project.
https://sourceforge.net/projects/opencvlibrary/files/opencv-win/3.2.0/opencv-3.2.0-vc14.exe/download

Please use the following code to execute the model.

cv::Ptr<cv::ml::RTrees> importXMLmodule_BT;

cv::Ptr<cv::ml::RTrees> importXMLmodule_HV;

importXMLmodule_BT = cv::Algorithm::load<cv::ml::RTrees>("Model_BT.xml");

importXMLmodule_HV = cv::Algorithm::load<cv::ml::RTrees>("Model_HV.xml");
