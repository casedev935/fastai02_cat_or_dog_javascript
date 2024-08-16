# fastai02_cat_or_dog_javascript

## Introduction

- This project aims to correctly classify a picture of a dog or cat. 
- This is a FASTAI course [Lesson #2](course.fastai.com) example that classifies whether the image is of a Dog or a Cat. 
- It uses Gradio's API to predict the image. All other code is done with html/javascript. 
- It then puts it into production via Github Pages, using FastPAGES. 
- Link to this project's [CatDogJavascript](https://huggingface.co/spaces/casedev/test/)
- It can also run locally just by opening index.html.

## Technologies used

[![Kaggle](https://www.vectorlogo.zone/logos/kaggle/kaggle-ar21.svg)](https://www.kaggle.com/)
[![Jupyter](https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg)](https://jupyter.org/) 
[![HuggingFace](https://seekvectorlogo.net/hugging-face-vector-logo-svg/)](https://huggingface.co/spaces/casedev/test/)
[![Gradio](https://github.com/gilbarbara/logos/blob/main/logos/gradio.svg)](https://www.gradio.app/)
[![FastAI](https://github.com/fastai/logos/blob/main/fastai_small.png)](https://www.fast.ai/)

## Requirements

- FASTAI VISION

## Training the Model

- CatOrDogTrainer.ipynb
- Trained in Kaggle Notebook
- Pretrained on CNN RESNET-18 
- Fine-tuned in 3 epochs
- Generated model.pkl

## Prediction the Outcome

- Prediction used with Gradio's API endpoint. 

- Gradio's API code snippet to fetch the prediction: 

```
client = Client("casedev/test")
result = client.predict(
		img=handle_file('image'),
		api_name="/predict"
)
print(result)
```

- Result's dictionary is in the following form:

```
Dict(label:       str | int | float | None, 
     
     confidences: List
     		[Dict(
     				label: str | int | float | None, 
     				confidence:  float | None)
     		] 

     		| None)
```



