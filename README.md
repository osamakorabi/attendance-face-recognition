# Face Recognition Entrance System

This project is a **Face Recognition Entrance System** that detects and logs people entering and leaving a monitored space using a webcam. It uses **OpenCV**, **face_recognition**, and **pandas** to track known individuals and record entry/exit events.

## Features
- Detects and recognizes faces from a predefined dataset.
- Logs entry and exit times automatically.
- Stores logs in a CSV file (`entrance.csv`).
- Displays real-time video feed with detected names.
- Prevents rapid alternating detections using a grace period.
- Works with a standard webcam.

## Installation
### Prerequisites
Ensure you have Python installed (recommended: Python 3.7+).

### Install Dependencies
Run the following command to install the required packages:
```sh
pip install opencv-python face-recognition pandas
```

## How to Use
1. **Prepare the Dataset:**
   - Create a `dataset` folder in the project directory.
   - Place labeled images of known individuals inside (e.g., `majd.jpg`, `mehdi.jpg`, `osama.jpg`).

2. **Run the Script:**
   ```sh
   python face_recognition_system.py
   ```

3. **Interacting with the System:**
   - The script will open a webcam feed.
   - Recognized faces will be logged as "Entered" or "Left."
   - Press `q` to exit the program.

4. **Check Logs:**
   - The system saves logs in `entrance.csv` in the format:
     ```csv
     Name,Event,Time
     majd,Entered,2025-03-05 12:30:15
     majd,Left,2025-03-05 12:45:10
     ```

## Configuration
- **Modify `image_files` and `names`** in the script to match your dataset.
- **Adjust the `grace_period`** to change the delay between alternating entries and exits.

## Dependencies
- `opencv-python`
- `face-recognition`
- `pandas`

## Future Improvements
- Enhance accuracy with additional face embeddings.
- Improve UI for better real-time visualization.
- Add a database for long-term logging.

## License
This project is open-source and available under the **MIT License**.

