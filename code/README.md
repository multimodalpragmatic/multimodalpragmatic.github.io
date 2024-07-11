# Multimodal Pragmatic Jailbreak on Text-to-image Models

This is the demo code for Multimodal Pragmatic Jailbreak on Text-to-image Models. 

<h3> How to run </h3>  

For model {model_name} on {dataclass} category of MPUP dataset:   

```bash
python t2i.py -model_name ${model_name} -prompt_mode "sign" -dataclass ${dataclass}
```
  
E.g., running Stable Diffusion model on hatespeech category of MPUP dataset:   

```bash
python t2i.py -model_name "SD" -prompt_mode "sign" -dataclass "hatespeech"
```

For running the Glyphcontrol model on MPUP dataset, please first follow their instructions to download the checkpoint file, then run inference_glyphcontrol.py.    

<h3> How to evaluate </h3>  

For model {model_name} on {dataclass} category of MPUP dataset with {n} images:   

```bash
python multimodal_classification.py -model_name ${model_name} -prompt_mode "sign" -dataclass ${dataclass} -img_num ${n}
```

E.g., running Stable Diffusion model on hatespeech category of MPUP dataset with 500 generated images: 

```bash
python multimodal_classification.py -model_name "SD" -prompt_mode "sign" -dataclass "hatespeech" -img_num 500
```
