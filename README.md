# Cricket Batting Analysis Tool
Analyzes cricket batting technique using computer vision and MediaPipe pose estimation to provide real-time biomechanical feedback.

## Features

Analyzes footwork, head position, swing control, balance, and follow-through<br>
Generates annotated videos with live feedback overlay<br>
Provides detailed scoring (1-10) for each aspect<br>
Creates comprehensive JSON analysis reports<br>

**Setup**
bash# Install system dependencies<br>
*sudo apt-get update && apt-get install -y ffmpeg*

## Install Python dependencies

*pip install -r requirements.txt*

## Usage

Update VIDEO_URL in the script with your YouTube video URL<br>

**Run the analysis:**
bash<br>
*python cricket_analysis.py*<br>

Check output files in ./output/:

**annotated_video.mp4 -** Video with feedback overlays<br>
**evaluation.json -** Detailed analysis report



## Configuration

Adjust biomechanical thresholds in the script:<br>
pythonGOOD_ELBOW_ANGLE = 120      # degrees<br>
GOOD_SPINE_LEAN = 15        # degrees from vertical<br>
GOOD_HEAD_KNEE_ALIGN = 40   # pixels<br>


## Assumptions

Clear side-on video showing full body of single batter<br>
Conventional cricket batting stance (left-handed analysis)<br>
Good lighting with minimal occlusion<br>
Internet connection for YouTube video downloads<br>
Standard video formats supported by OpenCV<br>

## Limitations

**2D analysis only -** cannot measure true 3D angles or depths<br>
**Generic thresholds -** doesn't account for individual body proportions<br>
**Shot type specific -** optimized for front-foot drives, may not suit all shots<br>
**Pose detection dependent -** accuracy varies with video quality and lighting<br>
**No outcome correlation -** analyzes technique, not shot effectiveness<br>
**Fixed camera perspective -** angle measurements affected by camera position<br>
