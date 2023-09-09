# llama7b-on-golem

Hello everyone, I have been trying to run Llama-7B on [golem.network](https://golem.network)

To get started with deployment of Llama-7B, lets first get started by running python on the golem network. You can follow the steps [here](https://github.com/golemfactory/golem-kernel-python), or below steps. I would recommend to follow below steps.

I expect you have python3 and pip installed.

## Get started with golem kernel python

Lets first start by creating a virtual env
```bash
python3 -m venv --clear ~/.envs/golem-kernel-python
source ~/.envs/golem-kernel-python/bin/activate
```
```bash
pip install jupyterlab
```

Yagna - version 0.12.2 or above
```bash
curl -sSf https://join.golem.network/as-requestor | bash -
```
Install Jupyter on Golem package from PyPI:
```bash
pip install jupyter-on-golem
```
Add jupyter-on-golem to the list of known kernels:
```bash
python -m jupyter_on_golem install
```
Jupyter on Golem needs Yagna running on Your host to be able to talk with Golem Network. You can run it with single command (preferably in the separate Console Window):
```bash
yagna service run 
```
With Yagna up and running You can start JupyterLab in standard fashion:
```bash
jupyter-lab
```
If installation process was completed correctly then Golem kernel should be visible and available in JupyterLab web interface:
![image](https://github.com/siddharth-sable/llama7b-on-golem/assets/66620788/7a0fbd74-d6e5-497f-a9f9-4b96cb0c18b9)

Choose the golem console from above image: then try,
```bash
%help
```
If you get below output, we are good to go
![image](https://github.com/siddharth-sable/llama7b-on-golem/assets/66620788/f171eedd-a448-400d-b5bb-bf19610f5093)

```bash
%status
```
Shows the current status of Jupyter on Golem.

Requests for Goerli testnet tokens: tGLM and tETH. You can only get Goerli testnet tokens this way.
```bash
%fund goerli
```
To setup for Goerli Testnet and Allocate 2 tGLM:
```bash
%budget goerli 1
```
Connect to the golem network (testnet):
```bash
%connect
```



