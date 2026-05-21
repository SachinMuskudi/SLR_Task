<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00B4DB,50:0083B0,100:005C97&height=240&section=header&text=Simple%20Linear%20Regression%20Web%20App&fontSize=42&fontColor=ffffff&animation=fadeIn&fontAlignY=38"/>

<h1>📈 Simple Linear Regression Prediction System</h1>

<p>
A Machine Learning Web Application built using 
<b>Python</b>, <b>Flask</b>, <b>Scikit-Learn</b>, 
<b>NumPy</b>, and <b>HTML</b>.
</p>

<p>
This project predicts output values using a trained 
<b>Simple Linear Regression Model</b> and provides 
real-time predictions through a clean Flask web interface.
</p>

<img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python"/>
<img src="https://img.shields.io/badge/Flask-Web%20Framework-black?style=for-the-badge&logo=flask"/>
<img src="https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?style=for-the-badge&logo=scikitlearn"/>
<img src="https://img.shields.io/badge/HTML-Frontend-red?style=for-the-badge&logo=html5"/>
<img src="https://img.shields.io/badge/NumPy-Numerical%20Computing-blueviolet?style=for-the-badge&logo=numpy"/>

</div>

<br><br>

<hr>

<h2>🚀 Project Overview</h2>

<p>
This project is a Machine Learning based prediction system 
that uses a trained <b>Simple Linear Regression Model</b> 
to make predictions based on user input.
</p>

<p>
The model is integrated with a Flask backend and deployed 
through a simple and interactive web interface where users 
can enter values and instantly receive predictions.
</p>

<hr>

<h2>🧠 Technologies Used</h2>

<table align="center" border="1" cellpadding="10">

<tr>
<th>Technology</th>
<th>Purpose</th>
</tr>

<tr>
<td>Python</td>
<td>Core Programming Language</td>
</tr>

<tr>
<td>Flask</td>
<td>Backend Web Framework</td>
</tr>

<tr>
<td>Scikit-Learn</td>
<td>Machine Learning Model</td>
</tr>

<tr>
<td>NumPy</td>
<td>Numerical Computations</td>
</tr>

<tr>
<td>Pickle</td>
<td>Model Serialization</td>
</tr>

<tr>
<td>HTML</td>
<td>Frontend User Interface</td>
</tr>

</table>

<hr>

<h2>📂 Project Structure</h2>

<div align="left">

<pre>
SLR_Task/
│
├── templates/
│   └── index.html
│
├── app.py
├── SLR_Task.pkl
├── requirements.txt
└── venv/
</pre>

</div>

<hr>

<h2>⚙️ Application Workflow</h2>

<ul>
<li>User enters input values in the web form.</li>
<li>Flask receives the request from the frontend.</li>
<li>The trained regression model processes the data.</li>
<li>The application generates predictions instantly.</li>
<li>The result is displayed back on the webpage.</li>
</ul>

<hr>

<h2>🖥️ Flask Application Explanation</h2>

<h3>📌 Importing Libraries</h3>

<div align="left">

<pre>
import flask
from flask import Flask, render_template, request
import numpy as np
import pickle
from sklearn.linear_model import LinearRegression
</pre>

</div>

<p>
These libraries are used for building the Flask web application,
handling requests, performing numerical operations, and loading
the trained machine learning model.
</p>

<hr>

<h3>📌 Loading the Trained Model</h3>

<div align="left">

<pre>
with open('SLR_Task.pkl', 'rb') as f:
    model = pickle.load(f)
</pre>

</div>

<p>
The trained Simple Linear Regression model is loaded using
Pickle for prediction purposes.
</p>

<hr>

<h3>📌 Creating Flask Application</h3>

<div align="left">

<pre>
app = Flask(__name__)
</pre>

</div>

<p>
Initializes the Flask application.
</p>

<hr>

<h3>📌 Home Route</h3>

<div align="left">

<pre>
@app.route('/')
def sample():
    return render_template('index.html')
</pre>

</div>

<p>
This route loads the homepage of the application.
</p>

<hr>

<h3>📌 Prediction Route</h3>

<div align="left">

<pre>
@app.route('/predict', methods=['GET', 'POST'])
def fun():
    a = [float(i) for i in request.form.values()]
    b = [np.array(a)]
    predictions = model.predict(b)
    predictions = predictions[0]

    return render_template(
        'index.html',
        prediction_text=predictions
    )
</pre>

</div>

<p>
This route receives user input, converts it into a NumPy array,
sends it to the trained regression model, and returns the
prediction result to the webpage.
</p>

<hr>

<h3>📌 Running Flask Server</h3>

<div align="left">

<pre>
if __name__ == '__main__':
    app.run(debug=True)
</pre>

</div>

<p>
Runs the Flask development server locally.
</p>

<hr>

<h2>📦 Installation</h2>

<h3>1️⃣ Clone Repository</h3>

<div align="left">

<pre>
git clone https://github.com/SachinMuskudi/SLR_Task.git
</pre>

</div>

<h3>2️⃣ Navigate to Project Folder</h3>

<div align="left">

<pre>
cd SLR_Task
</pre>

</div>

<h3>3️⃣ Install Dependencies</h3>

<div align="left">

<pre>
pip install -r requirements.txt
</pre>

</div>

<h3>4️⃣ Run Flask Application</h3>

<div align="left">

<pre>
python app.py
</pre>

</div>

<hr>

<h2>🌟 Features</h2>

<ul>
<li>Real-time Machine Learning Predictions</li>
<li>Simple and User Friendly Interface</li>
<li>Fast Flask Backend Integration</li>
<li>Beginner Friendly ML Project</li>
<li>Easy to Deploy</li>
<li>Lightweight Application Structure</li>
</ul>

<hr>

<h2>📚 Requirements</h2>

<div align="left">

<pre>
flask
numpy
scikit-learn
pickle-mixin
</pre>

</div>

<hr>

<h2>🚀 Future Improvements</h2>

<ul>
<li>Add Attractive UI Design</li>
<li>Deploy on Cloud Platforms</li>
<li>Add Prediction Graphs</li>
<li>Store Prediction History</li>
<li>Improve Input Validation</li>
<li>Add Database Integration</li>
</ul>

<hr>

<h2>👨‍💻 Author</h2>

<div align="center">

<h3>Sachin Muskudi</h3>

<p>
Passionate about Python, Machine Learning, Deep Learning,
NLP, Generative AI, Agentic AI, and Full Stack AI Applications.
</p>

<img src="https://img.shields.io/badge/Made%20With-Python-blue?style=for-the-badge&logo=python"/>
<img src="https://img.shields.io/badge/Machine-Learning-orange?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Flask-WebApp-black?style=for-the-badge&logo=flask"/>

</div>

<hr>

<div align="center">

<h2>⭐ If you like this project, give it a Star ⭐</h2>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:005C97,50:0083B0,100:00B4DB&height=150&section=footer"/>

</div>
