# Prompt Injection Simulator

A tool for evaluating the robustness of AI system prompts against prompt injection and jailbreak attacks.

## Overview

This application allows you to:

1. Test a system prompt against various attack prompts
2. Evaluate whether the AI model resists or fails under attack
3. Document and save test outcomes
4. Use a Safe Mode to pre-screen inputs for malicious patterns

## Features

- **System Prompt Testing**: Input your own system prompt or use the default one
- **Attack Prompt Library**: Comes with 5 pre-configured attack prompts, or add your own
- **Safe Mode**: Pre-screens user inputs for potentially malicious patterns
- **Results Tracking**: Records each test with detailed evaluation
- **Defense Recommendations**: Provides suggestions for improving prompt security

## Requirements

- Python 3.6+
- tkinter (usually comes with Python)
- requests library

## Installation

1. Make sure you have Python installed on your system
2. Install the required packages:
   ```
   pip install requests
   ```
3. Run the application:
   ```
   python prompt_injection_simulator.py
   ```

## Usage

1. Enter your OpenAI API key in the API Configuration section
2. Select the model you want to test (default is gpt-3.5-turbo)
3. Modify the system prompt if desired
4. Add or modify attack prompts in the Attack Prompts section
5. Enable or disable Safe Mode as needed
6. Click "Run Simulation" to start the tests
7. Review the results in the tabbed interface
8. Save results to a JSON file for further analysis

## Safe Mode

The Safe Mode feature pre-screens inputs for suspicious patterns such as:
- "ignore instructions"
- "forget instructions"
- "disregard constraints"
- "bypass"
- "override"
- "act like"
- "pretend"
- And other patterns that might indicate an attempt to manipulate the AI

## Defense Mechanisms

The application suggests several defense mechanisms:
1. **System prompt hardening**: Make your system prompt more specific and robust
2. **Input filtering**: Filter out known malicious patterns
3. **Risky pattern detection**: Identify and flag suspicious instructions
4. **Context freezing**: Prevent the model from forgetting its original instructions
5. **Conversation anchoring**: Regularly remind the model of its constraints

## License

This project is open source and available for educational and research purposes.

## Disclaimer

This tool is designed for educational and security research purposes only. Please use responsibly and in accordance with OpenAI's usage policies.
