import os
import openai

# Get API key from environment variable instead of hardcoding
openai.api_key = os.getenv("OPENAI_API_KEY")

response = openai.ChatCompletion.create(
    model="gpt-4o-mini",
    messages=[{"role":"user","content": "Write a motivational quote"}]
)
print(response.choices[0].message.content)
