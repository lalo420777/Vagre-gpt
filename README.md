211dfb860b7356256cd3ec503f9db7fa328c420aflask openai python-dotenvOPENAI_API_KEY=sk-tu_clave_aquípip install -r requirements.txt python vagre_gpt_app.pyhttps://github.com/lalo420777/Vagre-gpt/releases/tag/untagged-1c856d4c516a8607dd69a8b9b61aa73f753c8a50ac0af92eeb5cb81754f6b3ce31be7895ddf795943e94275a37b9a82e12b1pip install flask openai python vagre_gpt_app.py5eb1fe21938d9a42760f88ab7eb3f328ce76b06d1c90fe8c04b0287c27b3c0afb8425c08d500806a60362e253233930c74f00ba40196bf42import openai import os from flask import Flask, render_template_string, request from dotenv import load_dotenv

load_dotenv() openai.api_key = os.getenv("OPENAI_API_KEY")

app = Flask(name)

HTML_TEMPLATE = """

<title>Vagre GPT</title> <style> body { background-color: #121212; color: #ffffff; font-family: 'Courier New', monospace; padding: 40px; } input[type="text"] { width: 60%%; padding: 10px; border-radius: 8px; border: none; } button { padding: 10px 20px; background: #1e90ff; border: none; border-radius: 8px; color: white; font-weight: bold; cursor: pointer; } .chatbox { margin-top: 20px; padding: 20px; background: #1e1e1e; border-radius: 10px; } </style>
🤖 Vagre GPT
Enviar
{% if user_input %}
<div class="chatbox">
    <p><strong>Tú:</strong> {{ user_input }}</p>
    <p><strong>Vagre GPT:</strong> {{ vagre_output }}</p>
    <audio controls autoplay>
        <source src="https://api.voicerss.org/?key=demo&hl=es-mx&src={{ vagre_output | urlencode }}" type="audio/mpeg">
        Tu navegador no soporta audio.
    </audio>
</div>
{% endif %}
"""
def get_vagre_response(prompt): response = openai.ChatCompletion.create( model="gpt-4", messages=[ {"role": "system", "content": "Eres Vagre GPT, un asistente leal, directo y creativo."}, {"role": "user", "content": prompt} ] ) return response.choices[0].message.content.strip()

@app.route("/", methods=["GET", "POST"]) def index(): user_input = "" vagre_output = "" if request.method == "POST": user_input = request.form["message"] vagre_output = get_vagre_response(user_input) return render_template_string(HTML_TEMPLATE, user_input=user_input, vagre_output=vagre_output)

if name == "main": app.run(debug=True)2a60b74a# Vagre-gpt Inteligencia artificial 35bd201000dd294df56a63f79350eddd429c06d6 fe884d3afa3f06e2b5ac0a7ae91e4541f95cbc3660362e253233930c74f00ba40196bf422a60b74a211dfb860b7356256cd3ec503f9db7fa328c420aflask
openai
python-dotenvOPENAI_API_KEY=sk-tu_clave_aquípip install -r requirements.txt
python vagre_gpt_app.pyhttps://github.com/lalo420777/Vagre-gpt/releases/tag/untagged-1c856d4c516a8607dd69a8b9b61aa73f753c8a50ac0af92eeb5cb81754f6b3ce31be7895ddf795943e94275a37b9a82e12b1pip install flask openai
python vagre_gpt_app.py5eb1fe21938d9a42760f88ab7eb3f328ce76b06d1c90fe8c04b0287c27b3c0afb8425c08d500806a60362e253233930c74f00ba40196bf42import openai
import os
from flask import Flask, render_template_string, request
from dotenv import load_dotenv

load_dotenv()
openai.api_key = os.getenv("OPENAI_API_KEY")

app = Flask(__name__)

HTML_TEMPLATE = """
<!DOCTYPE html>
<html>
<head>
    <title>Vagre GPT</title>
    <style>
        body {
            background-color: #121212;
            color: #ffffff;
            font-family: 'Courier New', monospace;
            padding: 40px;
        }
        input[type="text"] {
            width: 60%%;
            padding: 10px;
            border-radius: 8px;
            border: none;
        }
        button {
            padding: 10px 20px;
            background: #1e90ff;
            border: none;
            border-radius: 8px;
            color: white;
            font-weight: bold;
            cursor: pointer;
        }
        .chatbox {
            margin-top: 20px;
            padding: 20px;
            background: #1e1e1e;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <h1>🤖 Vagre GPT</h1>
    <form method="POST">
        <input type="text" name="message" placeholder="Escribe algo..." required>
        <button type="submit">Enviar</button>
    </form>

    {% if user_input %}
    <div class="chatbox">
        <p><strong>Tú:</strong> {{ user_input }}</p>
        <p><strong>Vagre GPT:</strong> {{ vagre_output }}</p>
        <audio controls autoplay>
            <source src="https://api.voicerss.org/?key=demo&hl=es-mx&src={{ vagre_output | urlencode }}" type="audio/mpeg">
            Tu navegador no soporta audio.
        </audio>
    </div>
    {% endif %}
</body>
</html>
"""

def get_vagre_response(prompt):
    response = openai.ChatCompletion.create(
        model="gpt-4",
        messages=[
            {"role": "system", "content": "Eres Vagre GPT, un asistente leal, directo y creativo."},
            {"role": "user", "content": prompt}
        ]
    )
    return response.choices[0].message.content.strip()

@app.route("/", methods=["GET", "POST"])
def index():
    user_input = ""
    vagre_output = ""
    if request.method == "POST":
        user_input = request.form["message"]
        vagre_output = get_vagre_response(user_input)
    return render_template_string(HTML_TEMPLATE, user_input=user_input, vagre_output=vagre_output)

if __name__ == "__main__":
    app.run(debug=True)2a60b74a# Vagre-gpt
Inteligencia artificial 
35bd201000dd294df56a63f79350eddd429c06d6
fe884d3afa3f06e2b5ac0a7ae91e4541f95cbc3660362e253233930c74f00ba40196bf422a60b74a
