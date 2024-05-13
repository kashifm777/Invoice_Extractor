# Invoice Extractor
## Streamlit Web App

This Streamlit web app leverages Google's GenerativeAI service (Gemini Pro Vision) to extract information from invoices based on user prompts and image analysis.

## Run on Streamlit  
You can try this app on Streamlit:  
[YouTube Transcriber](https://youtube-transcriber-mk.streamlit.app)

### 1. Features:

- **Image Upload:** Upload an invoice image for analysis.
- **Text Prompt:** Provide additional context or specific questions about the invoice (optional).
- **Invoice Understanding:** Extract key details like items, prices, and totals using Gemini Pro Vision.

### 2. Requirements:

- Python 3.x
- Streamlit (`pip install streamlit`)
- `dotenv` library (`pip install python-dotenv`)
- Google Cloud Project with GenerativeAI API enabled ([https://cloud.google.com/ai/generative-ai](https://cloud.google.com/ai/generative-ai))
- Pillow library (`pip install Pillow`)

### 3. Setup:

1. Create a virtual environment (recommended): `python -m venv venv`
2. Activate the environment: `source venv/bin/activate` (Windows: `venv\Scripts\activate`)
3. Install dependencies: `pip install streamlit python-dotenv pillow`
4. Create a `.env` file in the project directory:
   - Add `GOOGLE_API_KEY=<YOUR_API_KEY>` (replace with your GenerativeAI API key)

### 4. Running the App:

1. Open a terminal in the project directory.
2. Run the app: `streamlit run app.py`
3. Access the app in your web browser at http://localhost:8501.

### 5. Usage:

1. Upload an invoice image.
2. (Optional) Provide a text prompt to specify what information you want to extract from the invoice.
3. Click the "Tell me about the image" button.

### 6. Output:

The app displays the extracted information from the invoice based on Gemini Pro Vision analysis and your input prompt (if provided). The working of this streamlit webapp is shown in the Screen shots below:  

#### 6.1. Case I:  

1. The user uploads the invoice:  

![invioce 1 uploaded](screen_capture/invoice_1_1.png)    
    
2. As shown in the above screen capture, the user asked who is this invoice billed to?  

3. When the prompt is passed, the system replies:  
   
![person billed](screen_capture/invoice_1_3.png)    

As shown in the screen capture above, the app generates the name and address of the person whom this invoice is billed to.  

#### 6.2. Case II:  

1. The user asks, "Payment is due in how many days?"  

![Payment timeline](screen_capture/invoice_1_4.png)    

2. The system replies with the number of days.  

![number of days](screen_capture/invoice_1_5.png)


### 7. Note:

- This is a basic example using a free-tier API. Invoice extraction accuracy may vary.
- Consider integrating with a reliable invoice parsing library for more structured data extraction.

### 8. Disclaimer:

This application and its output are for informational purposes only and should not be used for financial accounting or legal purposes. Always consult a qualified professional for accurate invoice analysis.
