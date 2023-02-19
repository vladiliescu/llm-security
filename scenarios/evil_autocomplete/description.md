This example shows how AI-based autocompletion engines can get confused about what code is executed and which is just documentation.
Most commercial AI autocompletion engines pull context from various locations; it is currently not known how to manipulate this more reliably or how to ensure we can always keep injections in the context window.
It may be that several such engines also don't pull context from external packages. However, this is an unaudited, proprietary process that is not well understood for available products.

Instructions:
Open autocomplete.py and put your cursor next to the print.
The print statement will behave just like normal, in face the loaded package does not load any code other than the statement print=print, which is not easily caught with existing testing, auditing or analysis tools.
Adversaries may inject arbitrary and subtle vulnerabilities into code if some part of the AI autocompletion context window 
contains untrusted content (documentation or code)