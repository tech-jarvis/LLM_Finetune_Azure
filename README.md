# Azure LLM Fine-tuning Guide

## Overview
Welcome to the Azure LLM Fine-tuning project! This repository provides a comprehensive guide for fine-tuning and deploying Large Language Models (LLMs) on Azure. We demonstrate the process using Microsoft's [Phi-3-mini-4k-instruct](https://huggingface.co/microsoft/Phi-3-mini-4k-instruct) model, though the approach works with any publicly licensed LLM from Hugging Face.

> **Important Notice**: For the latest official version, please visit https://github.com/Azure/azure-llm-fine-tuning

## Prerequisites

### Azure Resources
- Azure ML Workspace (you'll need your `<WORKSPACE_NAME>`, `<RESOURCE_GROUP>`, and `<SUBSCRIPTION_ID>`)
- [Azure ML CLI v2](https://learn.microsoft.com/en-us/azure/machine-learning/concept-v2?view=azureml-api-2#azure-machine-learning-cli-v2) installed

### Compute Requirements
1. **Development Environment**
   - Compute Instance: `Standard_DS11_v2`
   - Specs: 2 cores, 14GB RAM, 28GB storage
   - Purpose: Code development and testing

2. **Training Environment**
   - Recommended Options:
     - NVIDIA A100: `Standard_NC24ads_A100_v4`
     - NVIDIA V100: `Standard_NC6s_v3`
   - Note: Low-priority VMs are available for cost optimization

## Quick Start Guide

1. **Setup Development Environment**
   ```shell
   git clone https://github.com/tech-jarvis/LLM_Finetune_Azure.git
   conda activate azureml_py310_sdkv2
   pip install -r requirements.txt
   ```

2. **Project Structure**
   - `dataset-preparation/`: Tools and guides for data preprocessing
   - `fine-tuning/`: Core training and deployment scripts

3. **Training and Deployment**
   - Configure your settings in `fine-tuning/config.yml`
   - Choose your preferred approach:
     - **MLflow Pipeline** (Recommended):
       1. Run `1_training_mlflow.ipynb`
       2. Run `2_serving.ipynb`
     - **Custom Pipeline**:
       1. Run `1_training_custom.ipynb`
       2. Run `2_serving.ipynb`

## Additional Resources

### Technical References
- [Azure ML Examples Repository](https://github.com/Azure/azureml-examples)
- [Phi-3 Fine-tuning Tutorial](https://techcommunity.microsoft.com/t5/ai-machine-learning-blog/finetune-small-language-model-slm-phi-3-using-azure-machine/ba-p/4130399)
- [Phi-3 Model Variants](https://huggingface.co/daekeun-ml/Phi-3-medium-4k-instruct-ko-poc-v0.1)

### Legal and Contribution Guidelines

#### Contributing
We welcome community contributions! Before contributing:
1. Review our [Contributor License Agreement (CLA)](https://cla.opensource.microsoft.com)
2. Follow the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/)
3. For questions, contact [opencode@microsoft.com](mailto:opencode@microsoft.com)

#### Legal Information
- **License**: MIT-0 (see LICENSE file)
- **Trademarks**: Usage of Microsoft trademarks must comply with [Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general)