🎨 kas Image Generator

A simple AI Image Generator web application built with Python, Streamlit, and Hugging Face Diffusers.

The application allows users to enter a text prompt and generate an image using a text-to-image diffusion model.

✨ Features

📝 Enter a text prompt

🤖 Generate images using an AI diffusion model

🖼️ Display the generated image directly in the Streamlit app

⏳ Show a loading indicator while the image is being generated

🎨 Simple and easy-to-use interface

🛠️ Technologies Used

Python

Streamlit -- for the web interface

Hugging Face Diffusers -- for text-to-image generation

PyTorch -- used by the diffusion pipeline

Pillow -- for image handling


⚙️ Installation


Install the required libraries
pip install streamlit diffusers torch transformers pillow

Note: Image generation can require significant memory and processing power. A GPU can make generation considerably faster.

▶️ Run the Application

Run the following command inside the project folder:

streamlit run Image_Generator.py

🧑‍💻 How to Use

Start the Streamlit application.

Enter a description in the Enter your prompt text box.

Click Generate Image.

Wait while the AI model generates the image.

The generated image will appear below the button.

Example Prompt

A cute cat sitting in a garden

The application can generate an image based on the entered description.

🧠 How It Works

The application uses the Hugging Face Diffusers library to create a text-to-image pipeline:

pipe = DiffusionPipeline.from_pretrained("nota-ai/bk-sdm-tiny")

The user's prompt is passed to the pipeline:

image = pipe(prompt).images[0]

The generated image is then displayed using Streamlit:

st.image(image, caption="Generated Image")

🔄 Application Workflow

User enters prompt ↓ Click "Generate Image" ↓ Load text-to-image diffusion pipeline ↓ Send prompt to AI model ↓ Generate image ↓ Display generated image

📌 Example

Input:

A cute cat sitting in a garden

Output:

An AI-generated image based on the entered prompt.

🚀 Future Improvements

Possible improvements include:

Add image size controls

Add a negative-prompt field

Add generation settings such as steps and guidance scale

Add an option to download generated images

Add multiple image generation

Add image history

Improve the user interface

Add GPU/CPU selection

Add error handling for model-loading or generation failures

⚠️ Notes

The first run may take longer because the model needs to be downloaded.

Image generation performance depends on the computer's available CPU, GPU, and RAM.

The quality of generated images depends on the selected model and prompt.


GitHub Repository: https://github.com/kaszuk29-ship-it/Image_generator

📄 License

This project is intended for educational and demonstration purposes.
