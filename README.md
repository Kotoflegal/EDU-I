import requests

def generate_talking_avatar(video_params):
    api_url = "https://example.com/api/generate_talking_avatar"
    
    # Sudarome užklausos parametrus su duotais video_params
    payload = {
        "model_id": video_params["model_id"],
        "template_id": video_params["template_id"],
        "speaker_id": video_params["speaker_id"],
        # Kiti parametrai...
        "text": video_params["text"],
        # Kiti parametrai...
    }

    # Siunčiame užklausą į API
    response = requests.post(api_url, data=payload)

    # Gavus atsakymą, galime apdoroti rezultatus arba grąžinti, kaip reikia
    return response.text

# Pavyzdys kaip galėtų būti naudojamas funkcijos kvietimas:
video_params = {
    "model_id": "your_custom_avatar_id",
    "template_id": "your_custom_template_id",
    "speaker_id": "accent_model_id",
    # Kitos reikšmės...
    "text": "Jūsų video skriptas čia.",
    # Kitos reikšmės...
}

result = generate_talking_avatar(video_params)
print(result)
