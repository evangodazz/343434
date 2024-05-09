# Discord IP Logger & Image Blur Web App / image hosting

This is a Flask web application designed to serve two main functionalities: logging IP addresses via Discord webhooks and blurring images provided by URLs. It also integrates with Telegraph for file uploads and hosting.

## Features

- **IP Logging via Discord Webhooks**: This app can send IP addresses, along with additional location information, to a Discord channel of your choice using Discord webhooks.

- **Image Blurring**: Given an image URL, the app can apply a Gaussian blur filter to the image. This feature supports both static images and animated GIFs.

- **Telegraph Integration**: Files uploaded through the app are hosted on Telegraph, allowing for easy sharing of media content.

## Prerequisites

- Python 3
- Flask
- requests
- aiohttp
- Pillow (PIL)

## Installation

1. Clone this repository to your local machine:

   ```
   git clone https://github.com/your-username/your-repo.git
   ```

2. Install the required dependencies using pip:

   ```
   pip install -r requirements.txt
   ```
---
## Usage

1. Run the Flask application:

   ```
   python app.py
   ```
### app usage
2. Visit `http://localhost:5000` in your web browser to access the application.

3. Use the `/hidden-grabber` endpoint to access the IP logging feature. Make sure to set up a Discord webhook and provide the webhook token/url to enable logging.

## 

### script usage
 You can directly upload files to be hosted on Telegraph using the `/upload` endpoint.
 exemple : 
```python
import requests

url = 'http://localhost:5000/upload'
file_path = '/path/to/your/file.jpg'

with open(file_path, 'rb') as file:
    files = {'file': file}
    response = requests.post(url, files=files)

# Print the response content
print(response.json())
```
---
## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
