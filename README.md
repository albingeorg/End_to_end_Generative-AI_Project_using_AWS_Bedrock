# End to end Generative-AI Project using AWS_Bedrock

This project demonstrates how to build a simple multilingual chatbot using **AWS Bedrock**, **LangChain**, and **Streamlit**.  
The chatbot runs on top of the **Mistral 7B Instruct** model deployed via AWS Bedrock.

---

## 🚀 Features
- Uses **AWS Bedrock** runtime for LLM inference  
- Built with **LangChain** (`LLMChain` + `PromptTemplate`)  
- Simple **Streamlit UI** for interaction  
- Supports multiple languages (`English`, `Spanish`, `Hindi`)  
- Adjustable **temperature** for creativity control  

---

## 🛠️ Requirements
Make sure you have the following installed:

- Python 3.9+  
- Anaconda or venv for virtual environments  
- AWS CLI configured with Bedrock access  
- Python packages:
  ```bash
  pip install boto3 streamlit langchain
  ```

---

## 📂 Project Structure
```
.
├── main.py        # Streamlit app
├── README.md      # Project documentation
└── requirements.txt (optional)
```

---

## 🔑 AWS Setup
1. Ensure you have **AWS CLI** installed and configured:
   ```bash
   aws configure
   ```
   - Use a profile with **Bedrock Runtime permissions**  
   - Region must be set to `ap-south-1` (as in the code)  

2. Enable Bedrock access in your AWS account (Bedrock is region-locked).  

---

## ▶️ Running the App
1. Activate your environment.  
   Example (Anaconda):
   ```bash
   conda activate bedrock
   ```

2. Run the Streamlit app:
   ```bash
   streamlit run main.py
   ```

3. Open the app in your browser at:
   ```
   http://localhost:8501
   ```

---

## 📝 Example Usage
1. Select a language from the sidebar (`English`, `Spanish`, `Hindi`).  
2. Type your question in the sidebar text area.  
3. The chatbot will generate a response in the chosen language.  

---

## ⚙️ Customization
- Change the **LLM model** by editing:
  ```python
  model_id = "mistral.mistral-7b-instruct-v0:2"
  ```
  You can switch to other Bedrock-supported models (e.g., Claude, Titan).  

- Adjust **temperature** for more/less creative answers:
  ```python
  model_kwargs={"temperature": 0.7}
  ```

---

## 📌 Notes
- AWS Bedrock access must be enabled on your AWS account.  
- Mistral models don’t accept `max_gen_len`; only `temperature` is used.  
- Use `Ctrl+C` in terminal to stop the Streamlit server.  

---

