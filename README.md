# Screen Video Recorder

A lightweight Python-based screen recording tool that captures your entire screen and saves it as a video file. Built with OpenCV and PyAutoGUI for seamless, cross-platform screen recording.

## Features

- **Full Screen Recording**: Capture your entire display in real-time
- **Adjustable Frame Rate**: Control recording quality and file size by adjusting FPS
- **Easy-to-Use**: Simple command-line interface with minimal configuration
- **Cross-Platform**: Works on Windows, macOS, and Linux
- **Multiple Output Formats**: Save recordings as MP4, AVI, or other supported video formats
- **Lightweight**: Minimal dependencies with efficient resource usage

## Installation

### Prerequisites

- Python 3.7 or higher
- pip (Python package manager)

### Setup

1. Clone the repository:
```bash
git clone https://github.com/yourusername/screen-video-recorder.git
cd screen-video-recorder
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

## Requirements

The project uses the following Python libraries:

- **OpenCV** (`opencv-python`) - For video encoding and frame processing
- **PyAutoGUI** (`pyautogui`) - For capturing screenshots
- **NumPy** - For array operations (usually installed as OpenCV dependency)

See `requirements.txt` for exact versions.

## Usage

### Basic Recording

Run the script with default settings:
```bash
python screen_recorder.py
```

### Custom Configuration

You can specify output filename and frame rate:
```bash
python screen_recorder.py --output my_recording.mp4 --fps 30
```

### Command-Line Arguments

- `--output` or `-o`: Output video filename (default: `recording.mp4`)
- `--fps` or `-f`: Frames per second for recording (default: 20)
- `--duration` or `-d`: Recording duration in seconds (leave blank for manual stop)

### Example

```bash
python screen_recorder.py -o gameplay.mp4 -f 30 -d 60
```

This records 60 seconds of your screen at 30 FPS and saves it as `gameplay.mp4`.

## How It Works

The recorder operates by:

1. **Screen Capture**: PyAutoGUI captures screenshots of your entire display at regular intervals
2. **Frame Encoding**: OpenCV encodes these screenshots into a video stream using the specified codec
3. **Video Output**: The encoded frames are written to a video file in your chosen format

This approach ensures compatibility across different operating systems while maintaining reasonable performance.

## Performance Considerations

- **FPS Impact**: Higher FPS values result in smoother videos but consume more CPU and disk space. 20-30 FPS is recommended for most use cases.
- **Resolution**: Recording at higher resolutions (1440p+) may impact performance on older machines. Consider your system specs before adjusting settings.
- **CPU Usage**: Screen recording is CPU-intensive. Close unnecessary applications for optimal performance.
- **File Size**: A 1-hour recording at 20 FPS can be 500MB-2GB depending on resolution and codec.

## Limitations

- **No Audio Recording**: The current version captures video only. Audio recording is not supported.
- **No Real-Time Compression**: Large videos are generated during recording; ensure sufficient disk space.
- **Single Monitor Only**: Currently records from the primary display only.
- **Performance Dependent**: Recording speed depends on your system's CPU and GPU capabilities.

## Troubleshooting

**Q: The video is lagging or stuttering**
- Reduce the FPS value or close other applications consuming CPU

**Q: Recording uses too much disk space**
- Decrease FPS or consider compressing the output file after recording

**Q: Getting permission errors on macOS**
- Grant accessibility permissions: System Preferences → Security & Privacy → Accessibility

## Future Improvements

- Audio recording capability
- GUI interface for easier configuration and recording controls
- Multi-monitor support
- Real-time video compression options
- Pause/resume recording functionality
- Region-specific recording (record only a portion of the screen)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Author

Created as a practical Python project exploring computer vision and screen automation libraries.

## Contributing

Contributions are welcome! If you have suggestions for improvements or encounter bugs, feel free to open an issue or submit a pull request.

---

**Happy recording!** 🎥
