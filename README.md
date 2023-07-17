# LangChain

This code repo helps to understand the basics of LangChain.

Prompt templates:

Most LLM applications do not pass user input directly into an LLM. Usually, they will add the user input to a larger piece of text, called a prompt template, that provides additional context on the specific task at hand.

Chains:

Chains help you to combine a model and a prompt template. Chains give us a way to link (or chain) together multiple primitives, like models, prompts, and other chains.

Agents:

To handle complex workflows, we need to be able to dynamically choose actions based on inputs. Agents help you to do this. Agents use a language model to determine which actions to take and in what order. Agents are given access to tools, and they repeatedly choose a tool, run the device, and observe the output until they come up with a final answer. These tools are function that performs a specific duty. This can be things like Google Search, Database lookup, Python REPL, other chains

Memory:

The chains and agents are stateless, but for many applications, it's necessary to reference past interactions. For example, chatbots, where you want to understand new messages in the context of past messages. The Memory module gives you a way to maintain the application state. The base Memory interface is simple: it lets you update the state given the latest run inputs and outputs and it enables you to modify (or contextualize) the following input using the stored state. There are many built-in memory systems. The simplest of these is a buffer memory which just prepends the last few inputs/outputs to the current input.
