import os

print(os.environ.get("GEMINI_API_KEY"))

from google import genai

client = genai.Client()

response = client.models.generate_content_stream(
    model="gemini-2.5-flash",
    contents="",

)

for chunk in response:
    print(chunk.text, end="")


API Key  -"AIzaSyAXXs8vZbf7DYo4qEodfGHdlGp7vFh_xao" 
