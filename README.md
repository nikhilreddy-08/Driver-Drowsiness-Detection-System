## Project Overview
Drowsy driving is a significant cause of traffic accidents worldwide. The **Driver Drowsiness Detection System** aims to enhance road safety by leveraging machine learning and computer vision to detect and alert drivers showing signs of fatigue in real-time. This project utilizes **Dlib** and **OpenCV** libraries in Python for robust facial landmark detection and blink analysis.

## Key Features
- **Real-Time Monitoring**: Continuous monitoring of the driver’s facial expressions using a dashboard-mounted camera.
- **Facial Landmark Detection**: Leverages Dlib's pre-trained 68-point facial landmark detector.
- **Eye Aspect Ratio (EAR) Analysis**: Tracks blinking patterns to determine alertness levels.
- **Dynamic Feedback**: Provides instant visual and auditory alerts for driver drowsiness.
- **User-Friendly Interface**: Offers real-time annotated video feeds with driver status updates.

## Technology Stack
- **Programming Language**: Python
- **Libraries**: OpenCV, Dlib, NumPy, Imutils
- **Hardware**: Camera for video input

## System Architecture
```plaintext
Camera Input -> Face Detection -> Facial Landmark Detection -> EAR Calculation -> Drowsiness Detection -> Alerts
```

### EAR Calculation Formula:
```
EAR = (|P2 - P6| + |P3 - P5|) / (2 * |P1 - P4|)
```
Where P1 to P6 are coordinates of specific facial landmarks around the eye.

## Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/username/driver-drowsiness-detection.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Download the **shape_predictor_68_face_landmarks.dat** file and place it in the project directory.
4. Run the application:
   ```bash
   python drowsiness_detection.py
   ```


## Future Enhancements
- **Integration with Vehicle Systems**: Connect with vehicle controls to trigger emergency measures.
- **Multi-Modal Data Fusion**: Incorporate additional sensors like EEG for more accurate detection.
- **Environmental Adaptation**: Enhance performance under varying lighting and weather conditions.
- **Advanced Alerts**: Add seat vibrations and notifications to emergency contacts.

