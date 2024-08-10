# local-gpt
Repo containing a basic setup to run GPT locally using open source models.

## Local Model With Open WebUI
1. Navigate to https://ollama.com and download ollama.
2. Once installed, download a model to use.
   - `ollama pull <model>` where `<model` is the model name from the Ollama models.
   - (Example: `ollama pull llama3.1`)
3. Ensure docker is installed by running `docker help`. If not installed, [download docker desktop](https://www.docker.com/products/docker-desktop/). After installing, run docvker desktop to ensure the docker engine is running.
4. Start up Open WebUI by running the following command:
  - `docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main`
5. Navigate to `http://localhost:3000`. You'll be presented with a login screen for Open WebUI.
6. Sign in or create an account. After completed, you will be redirected to the chat window where we can select the desired model and begin chatting!
