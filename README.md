# Custom Image Generator for Social Media Posts

This project is designed

## Requirements

- Python 3.x
- Dependencies: `Pillow`

## Installation

1. Clone this repository to your local machine:

```cmd
git clone https://github.com/waptechmx/quote-maker.git
```

## Usage
1. Ensure you have the required text and image files in the appropriate directories.
2. Adjust the configuration parameters according to your preferences.
3. Run the script.

```python
python main.py
```

Custom videos will be generated in the customers folder.

## Configuration

- TOPIC: The topic for which you want to generate images (fitness or christian).
- SHOW_AUTHOR: Set to True if you want to display the author of the quote under the quote.
- CUSTOMER_NAME: Your name or the customer's name.
- NUM_OF_POSTS: Number of posts to generate. Set to -1 to disable the limit.


## Creating a New Topic
To create a new topic, follow these steps:

- Create a {topic}.txt file inside the /sources/text_data directory.
- Run helper.create_new_topic_dirs(TOPIC, project_dir) to automatically create all the required directories.
- Add images to /sources/images/{topic}.
- Run helper.cut_images_new(images_folder, images_folder_cropped) to crop the images to 1080x1350 (you can change the dimensions inside the function).
- Run helper.darken_images(images_folder_cropped, images_folder_cropped_darken) if you want to make the images darker (it makes the text look better).

Feel free to create a Pull Request if you want to help others as well!

## Notes
Ensure you have ffmpeg tool installed and accessible in your system's PATH.
This project uses the ffmpeg-python package to interact with ffmpeg from Python.
It's assumed that the current directory is the project directory when running the script.