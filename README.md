```markdown
# Vimeo-Downloader

Vimeo-Downloader is a Python script that allows you to download Vimeo videos efficiently using the [yt-dlp](https://github.com/yt-dlp/yt-dlp) library. The script reads video URLs and optional passwords from a text file, downloads the videos in batches, and organizes the output in a specified folder.

## Features

- Batch download Vimeo videos with customizable options.
- Support for video passwords.
- Configurable output folder and download format.
- Utilizes the yt-dlp library for enhanced video downloading.

## Prerequisites

Before using the Vimeo-Downloader script, make sure you have the following installed:

- Python 3.x
- [yt-dlp](https://github.com/yt-dlp/yt-dlp)
- [aria2](https://aria2.github.io/) (external downloader)

Install the required Python packages using the following command:

```bash
pip install -r requirements.txt
```

## Usage

1. Create a text file (`add_vimeo_links.txt`) containing Vimeo video URLs and optional passwords in the following format:

   ```plaintext
   https://vimeo.com/123456789::your_password
   https://vimeo.com/987654321
   ```

2. Update the yt-dlp options in `main.py` as needed, especially the "referer" parameter.

3. Run the script:

   ```bash
   python main.py
   ```

   The script will process the video URLs in batches, downloading the videos and saving them in the specified output folder.

## Configuration

Adjust the configuration in `main.py` to customize the script:

- `file_path`: Path to the file containing video URLs and passwords.
- `output_folder`: Output folder for downloaded MP4 files.
- `batch_size`: Number of links to download at a time.
- `yt_dlp_options`: Options for the yt-dlp library (e.g., format, referer, external downloader settings).

## License

This script is licensed under the [MIT License](LICENSE).

## Acknowledgments

- [yt-dlp](https://github.com/yt-dlp/yt-dlp): Enhanced version of youtube-dl.
```