# AgentDos
Some projects related to DOS in AI Agents: 
- AutoDoS: https://github.com/shuita2333/AutoDoS
- PoisonedRAG: https://github.com/sleeepeer/PoisonedRAG
- pallms: https://github.com/mik0w/pallms
- AdvLLM: https://github.com/zqzqz/AdvLLM
---

# AutoDoS
> Crabs: Consuming Resrouce via Auto-generation for LLM-DoS Attack under Black-box Settings
## Initalization
Create a virtual environment and install the required packages:
```bash
git clone https://github.com/shuita2333/AutoDoS.git
cd AutoDoS
conda create -n autodos python=3.9 -y
conda activate autodos
pip install -r requirements.txt
unset ALL_PROXY
unset all_proxy
```
Add your API key to `API_key.py` in the root directory:
```python
# Calling GPT from "openAI"
OPENAI_API_KEY=""
OPENAI_BASE_URL=""

# Calling Qwen and Llama from "https://www.aliyun.com/"
# ALIYUN_API_KEY = ""
# ALIYUN_BASE_URL = "https://dashscope.aliyuncs.com/compatible-mode/v1"

# Calling Ministral from platform "https://mistral.ai/"
# Mistral_API = ""
# Mistral_BASE_URL = "https://api.mistral.ai/v1/chat/completions"

# Calling DeepSeek from "https://api.deepseek.com"
# DEEPSEEK_API_KEY = ""
# DEEPSEEK_BASE_URL = "https://api.deepseek.com/beta"

# Calling other models from platform "https://siliconflow.cn/"
# Siliconflow_API_KEY="""
# Siliconflow_BASE_URL= "https://api.siliconflow.cn/v1/chat/completions"
```
## Launcher
To launch the attack, run the following command:
```bash
python professional_iterative_generation.py --attack-model gpt-4o --target-model gpt-4o-mini --judge-model gpt-4o-mini --target-max-n-tokens 4096
```

General usage:
```bash
python professional_iterative_generation.py --attack-model [ATTACK MODEL] --target-model [TARGET MODEL] --judge-model [JUDGE MODEL] --function-descript [Application environment of target model] --target-max-n-tokens [max output length]
```

