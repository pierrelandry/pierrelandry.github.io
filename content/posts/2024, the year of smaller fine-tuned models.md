

At the end of 2022, OpenAI started the LLM revolution with the release of its own model, ChatGPT. When it was released, it outperformed the best open source model, BLOOM, by 90% on the MMLU test. Today, just over a year later, the delta between the best open source model (Mixtral-8x7b) and the best closed source model (GPT-4) [is around 15%](https://huggingface.co/spaces/lmsys/chatbot-arena-leaderboard) on the MMLU test. 2023 was the year of the explosion of open source models, led by the [LLaMA](https://ai.meta.com/blog/large-language-model-llama-meta-ai/) model used by Meta. This movement has led the open source community to work massively on deploying these models, giving rise to projects such as [llama.cpp] (https://github.com/ggerganov/llama.cpp), the main aim of which is to deploy the LLaMA model on MacBooks.
However, deploying a model comes with its own set of challenges.

**The challenge of open source models

- The cost of deployment
The biggest cost of deploying open source models is inference. The larger the model, the more processing power and memory it requires, and the more expensive it is, both financially and in terms of latency. These models are often deployed on expensive infrastructure that is not accessible to everyone (such as GPUs).

- Performance
There are two aspects to the performance of an LLM server: 
	- **Latency**: The time it takes for the model to generate a response for a user.
	- **Throughput**: The number of tokens an inference LLM server can generate per second.
We also need to monitor the performance of the model in terms of the relevance of its responses.

- Fine-tuning
While the largest models generally perform better on general tasks, they sometimes [hallucinate](https://en.wikipedia.org/wiki/Hallucination_(artificial_intelligence)) on more specific tasks.  To overcome this problem, the model can be fine-tuned to improve its performance on these specific tasks. Fine-tuning a small model for a more specific task can be a viable alternative to the cost of fine-tuning a larger model.

To reduce costs, it is better to use a smaller model than a larger one. This may be at the expense of performance. The performance levels of smaller models are often acceptable in the majority of use cases. A trade-off must be made between performance and cost of service. 

**Conclusion** : 
2023 was the year of open source AI (with LLaMA leading the way), with performance increasingly approaching that of proprietary models. For example, the open source mixtral-8x7b model performs [better](https://huggingface.co/spaces/lmsys/chatbot-arena-leaderboard) than ChatGPT (GPT-3.5-Turbo) on the [MMLU] test(https://arxiv.org/abs/2009.03300).
However, deploying these models is expensive in terms of infrastructure. More and more initiatives like llama.cpp are emerging to deploy these models on *commodity hardware*. 
To reduce costs, we prefer to go to smaller, fine-tuned models, sometimes at the expense of performance (acceptable for most enterprise use cases). 

So 2024 will be the year of the smallest models, open source fine-tuned for specific tasks and deployed on commodity hardware.