# adk_tool_agent

This is a tool agent which uses Google ADK with ollama model.

## Installation

To install this repo, follow there steps:

1. Clone the repository:

    $ git clone https://github.com/mutse/adk_tool_agent.git
    $ cd adk_tool_agent

2. Install the required dependencies:

    $ brew install uv  # for MacOS
    $ uv venv
    $ source .venv/bin/activate
    $ uv add google-adk litellm

## Usage

1. Navigate to the project directory:

    $ cd adk_tool_agent

2. Change to the directory of too\_agent, and copy env.example as .env:

    $ cp env.example .env

3. Modify the variables of `$HOST` and `$PORT` for your local ollama url:

    OPENAI_BASE_URL=http://$HOST:$PORT/v1
    OPENAI_API_KEY=ollama
    CHAT_MODEL=llama3.2:3b

4. Navigate to the project directory:

    $ cd ..

5. Run the agent:

    $ adk run tool_agent
    Log setup complete: /var/folders/gz/n243fjbn1pqbtm6dpx640crc0000gn/T/agents_log/agent.20250416_211728.log
    To access latest log: tail -F /var/folders/gz/n243fjbn1pqbtm6dpx640crc0000gn/T/agents_log/agent.latest.log
    Running agent weather_time_agent, type exit to exit.
    user: What is the time of New york?
    21:18:07 - LiteLLM:INFO: utils.py:3085 - 
    LiteLLM completion() model= llama3.2:3b; provider = openai
    21:18:12 - LiteLLM:INFO: cost_calculator.py:636 - selected model name for cost calculation: openai/llama3.2:3b
    21:18:12 - LiteLLM:INFO: cost_calculator.py:636 - selected model name for cost calculation: openai/llama3.2:3b
    21:18:12 - LiteLLM:INFO: utils.py:3085 - 
    LiteLLM completion() model= llama3.2:3b; provider = openai
    21:18:12 - LiteLLM:INFO: cost_calculator.py:636 - selected model name for cost calculation: openai/llama3.2:3b
    21:18:12 - LiteLLM:INFO: cost_calculator.py:636 - selected model name for cost calculation: llama3.2:3b
    21:18:13 - LiteLLM:INFO: cost_calculator.py:636 - selected model name for cost calculation: openai/llama3.2:3b
    21:18:13 - LiteLLM:INFO: cost_calculator.py:636 - selected model name for cost calculation: openai/llama3.2:3b
    [weather_time_agent]: The current time in New York is 9:18 AM EDT.
    user: What is the weather of New york?
    21:19:22 - LiteLLM:INFO: utils.py:3085 - 
    LiteLLM completion() model= llama3.2:3b; provider = openai
    21:19:22 - LiteLLM:INFO: cost_calculator.py:636 - selected model name for cost calculation: openai/llama3.2:3b
    21:19:22 - LiteLLM:INFO: cost_calculator.py:636 - selected model name for cost calculation: llama3.2:3b
    21:19:24 - LiteLLM:INFO: cost_calculator.py:636 - selected model name for cost calculation: openai/llama3.2:3b
    21:19:24 - LiteLLM:INFO: cost_calculator.py:636 - selected model name for cost calculation: openai/llama3.2:3b
    21:19:24 - LiteLLM:INFO: utils.py:3085 - 
    LiteLLM completion() model= llama3.2:3b; provider = openai
    21:19:24 - LiteLLM:INFO: cost_calculator.py:636 - selected model name for cost calculation: openai/llama3.2:3b
    21:19:24 - LiteLLM:INFO: cost_calculator.py:636 - selected model name for cost calculation: llama3.2:3b
    21:19:25 - LiteLLM:INFO: cost_calculator.py:636 - selected model name for cost calculation: openai/llama3.2:3b
    21:19:25 - LiteLLM:INFO: cost_calculator.py:636 - selected model name for cost calculation: openai/llama3.2:3b
    [weather_time_agent]: The current weather in New York is sunny, with a comfortable temperature of 25°C (41°F).
    user: exit

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
