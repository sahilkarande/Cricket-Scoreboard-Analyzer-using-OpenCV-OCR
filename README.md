# Cricket Scoreboard Analyzer using OpenCV & OCR

## Overview
This project aims to automate the extraction and analysis of cricket match statistics displayed on scoreboards from images or video frames. The system utilizes **OpenCV** for image processing and **Tesseract OCR** for text recognition to capture data such as runs, wickets, overs, and more. The project then performs basic statistical analysis and visualizes the data in graphical formats.

## Features
- **Scoreboard Detection**: Identifies the area in the image or video frame that contains the scoreboard.
- **OCR-Based Text Extraction**: Uses Tesseract OCR to extract text data from the detected scoreboard.
- **Basic Cricket Analysis**: Calculates statistics such as the run rate, wickets, and overs.
- **Visualization**: Displays the data through graphs (run rate, wickets over time, etc.).
- **User Interface (Optional)**: A simple interface to display extracted data and stats.

## Technologies Used
- **Python**: Programming language used for the implementation.
- **OpenCV**: For image processing tasks like scoreboard detection, cropping, and frame extraction.
- **Tesseract OCR**: For optical character recognition to extract text from the scoreboard.
- **Pandas**: For handling and analyzing extracted data.
- **Matplotlib**: For visualizing cricket statistics.
- **Tkinter** or **Streamlit** (Optional): For building a simple user interface.

## Setup & Installation

### Prerequisites:
Before running the project, ensure that you have the following installed:
- **Python** (Version 3.x)
- **Pip** (Python package manager)

### Step 1: Clone the Repository
Clone this repository to your local machine:
```bash
git clone https://github.com/yourusername/cricket-scoreboard-analyzer.git
cd cricket-scoreboard-analyzer
```

### Step 2: Install Dependencies
Install the required Python libraries:
```bash
pip install -r requirements.txt
```

### Step 3: Install Tesseract OCR
Tesseract OCR is an external dependency. You can install it from the following links:
- **Windows**: Download from [Tesseract OCR Installer](https://github.com/UB-Mannheim/tesseract/wiki)
- **Mac**: `brew install tesseract`
- **Linux**: `sudo apt-get install tesseract-ocr`

Ensure that Tesseract is accessible from your command line by adding its installation path to your system’s environment variables.

### Step 4: Run the Application
To run the application, simply execute the following:
```bash
python main.py
```

For video input, place the video file in the same directory and specify the file path in the script.

## How It Works

### 1. **Image Preprocessing**:
- The input image or video frame is preprocessed (converted to grayscale, noise removal, thresholding) to enhance the clarity for OCR.

### 2. **Scoreboard Detection**:
- OpenCV is used to detect the region of the image or frame where the scoreboard is located. It applies contour detection or template matching to extract the scoreboard section.

### 3. **Text Extraction**:
- Tesseract OCR reads the text from the detected scoreboard region. It extracts match-related data, such as runs, wickets, overs, etc.

### 4. **Data Parsing**:
- The extracted text is cleaned and parsed into meaningful information (runs, wickets, overs, etc.) using Python string manipulation or regular expressions.

### 5. **Basic Analysis**:
- The system performs basic cricket analysis, such as calculating the **current run rate** (Runs / Overs) and other metrics.
  
### 6. **Visualization**:
- Using Matplotlib, the system visualizes the extracted data as graphs, such as:
  - **Run rate over time**.
  - **Wickets count** during the match.

### 7. **User Interface** (Optional):
- If implemented, the user interface (using Tkinter or Streamlit) displays the match data in an easy-to-read format, including live score and analysis charts.

## Project Flow

1. **Preprocess Image/Video**: Convert to grayscale, clean the image for better OCR performance.
2. **Detect Scoreboard Area**: Use OpenCV to find the region containing the scoreboard.
3. **Extract Text**: Apply Tesseract OCR to extract data from the scoreboard.
4. **Parse Data**: Convert the OCR output into structured statistics (runs, wickets, overs).
5. **Analyze Data**: Calculate key statistics like run rate, and detect team performance trends.
6. **Visualize Data**: Plot graphs (run rate, wickets, etc.) using Matplotlib.
7. **Display Results**: (Optional) Show results on a user interface.

## Example
Here’s an example of how the application works:

**Input Image**:  
![Sample Cricket Scoreboard](path-to-image.png)

**Extracted Data**:  
- Runs: 120  
- Wickets: 3  
- Overs: 15

**Basic Analysis**:  
- Run Rate = 120 / 15 = 8.00

**Visualization**:  
A line graph showing the **Run Rate** over the course of the match.

## Challenges & Future Improvements
- **Text Accuracy**: OCR accuracy can be affected by poor image quality or different scoreboard formats. More advanced OCR techniques or training Tesseract with custom fonts may improve accuracy.
- **Real-Time Processing**: Implementing live video processing to track scores in real time would require optimizing frame processing.
- **Handling Diverse Scoreboards**: Different broadcasters use different scoreboard layouts, so improving the detection method for various formats would be a useful enhancement.

## Future Enhancements
- **Advanced Player Analysis**: Track individual player performances (e.g., batting, bowling).
- **Predictive Analytics**: Use historical data to predict the outcome of the match based on live data.
- **Real-Time Video Integration**: Implement live video processing for automated live match analysis.
- **Advanced User Interface**: Enhance the GUI with additional features like match commentary or predictions.

## Contributing
Feel free to fork this repository and submit issues or pull requests if you have suggestions for improvements or new features.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

### Sources:
- [OpenCV Documentation](https://docs.opencv.org/)
- [Tesseract OCR Documentation](https://tesseract-ocr.github.io/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [Python OpenCV Tutorials](https://docs.opencv.org/master/d9/df8/tutorial_root.html)
- [Tesseract OCR with Python](https://realpython.com/recognizing-text-with-ocr-in-python/)
