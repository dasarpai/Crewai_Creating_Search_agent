# BlogCreation Crew

Welcome to the BlogCreation Crew project, powered by [crewAI](https://crewai.com). This template is designed to help you set up a multi-agent AI system with ease, leveraging the powerful and flexible framework provided by crewAI. Our goal is to enable your agents to collaborate effectively on complex tasks, maximizing their collective intelligence and capabilities.

## Hari's Note to Run this sucessfull on local.

### Setup and Run LLM Server
- install ollama 
- download ollama3.1:8b
- run command: ollama run ollama3.1:8b
- create folder for experiment (crewai)

### Setup CrewAI Environment
- go to command terminal with admin permission
- python -m venv .venv 
- activate virtual environment
```
./venv/Script/activate
```
- #Install the mains CrewAI package
```
pip install crewai
```
- crewai create crew blog_creation
- cd blog_creation # Within this folder you will find your initial crew project structure
```
main files are 
- src/your_project_name/config/agents.yaml to define your agents
- src/your_project_name/config/tasks.yaml to define your tasks
- src/your_project_name/tools/custom_tool.py example of a custom tool
- src/your_project_name/crew.py to add your own logic, tools and specific args
- src/your_project_name/main.py runs your crew locally.
- src/your_project_name/.env holds your environment variables
```

- #Install the main CrewAI package and the tools package that includes a series of helpful tools for your agents
```
pip install crewai[tools]
```
- Install dependencies
```
pip install poetry
poetry install
```

### Set Environment Variables 
- src/your_project_name/.env (this file will have your environment variables. Since creating blog_creation i chose ollama model so that information is inside. Change the model name to ollama3.1:8b)

#### Setup SerpAPI
- Create account on serper.dev and generate an API. 
https://serper.dev/api-key
- set that api_key in .env file
```
SERPER_API_KEY = ""
```

### Run the Agent
- run crew locally
```
crewai run
or
crewai run blog_creation
```
In the main.py there is a script
```
def test():
    """
    Test the crew execution and returns the results.
    """
    inputs = {
        "topic": "Quantum Computing & Blockchain"
```
crewai run will run this test and throw a detail report prepared by the agents on "Quantum Computing & Blockchain"

## Installation (Provided by CrewAI)

Ensure you have Python >=3.10 <3.13 installed on your system. This project uses [UV](https://docs.astral.sh/uv/) for dependency management and package handling, offering a seamless setup and execution experience.

First, if you haven't already, install uv:

```bash
pip install uv
```

Next, navigate to your project directory and install the dependencies:

(Optional) Lock the dependencies and install them by using the CLI command:
```bash
crewai install
```
### Customizing

**Add your `OPENAI_API_KEY` into the `.env` file**

- Modify `src/blog_creation/config/agents.yaml` to define your agents
- Modify `src/blog_creation/config/tasks.yaml` to define your tasks
- Modify `src/blog_creation/crew.py` to add your own logic, tools and specific args
- Modify `src/blog_creation/main.py` to add custom inputs for your agents and tasks

## Running the Project

To kickstart your crew of AI agents and begin task execution, run this from the root folder of your project:

```bash
$ crewai run
```

This command initializes the blog_creation Crew, assembling the agents and assigning them tasks as defined in your configuration.

This example, unmodified, will run the create a `report.md` file with the output of a research on LLMs in the root folder.

## Understanding Your Crew

The blog_creation Crew is composed of multiple AI agents, each with unique roles, goals, and tools. These agents collaborate on a series of tasks, defined in `config/tasks.yaml`, leveraging their collective skills to achieve complex objectives. The `config/agents.yaml` file outlines the capabilities and configurations of each agent in your crew.

## Support

For support, questions, or feedback regarding the BlogCreation Crew or crewAI.
- Visit our [documentation](https://docs.crewai.com)
- Reach out to us through our [GitHub repository](https://github.com/joaomdmoura/crewai)
- [Join our Discord](https://discord.com/invite/X4JWnZnxPb)
- [Chat with our docs](https://chatg.pt/DWjSBZn)

Let's create wonders together with the power and simplicity of crewAI.
