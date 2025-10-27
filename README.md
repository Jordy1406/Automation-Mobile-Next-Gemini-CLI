# 📱 AI Mobile QA Agent: Shopping Automation on Shopee (Gemini CLI + Mobile Next MCP)

## 🚀 Quick Start: Installation and Usage

This project demonstrates how to orchestrate complex mobile application test flows using natural language commands, powered by the **Gemini CLI** agent and the **Mobile Next MCP** server. We use **scrcpy** to mirror and visualize the automation process on the desktop.

### 1. Install Gemini CLI & Configure the Agent

First, ensure you have the Gemini CLI installed and configured to recognize the Mobile Next MCP tool.

```bash
# 1. Install Gemini CLI globally
npm install -g @google/gemini-cli

# 2. Authenticate (required for Gemini access)
gemini
# Choose 'Login with Google' when prompted.
2. Configure Mobile Next MCP
You must add the Mobile Next MCP server configuration to your Gemini CLI settings file, typically located at ~/.gemini/settings.json.
Create or edit ~/.gemini/settings.json and add the following JSON block:
code
JSON
{
  "mcpServers": {
    "mobile-mcp": {
      "command": "npx",
      "args": ["-y", "@mobilenext/mobile-mcp@latest"]
    }
  }
}
3. Prepare Your Mobile Environment and Visualization (scrcpy)
You need a device (real or emulator) connected and a way to view the automation.
Prerequisites Check:
Ensure an Android Emulator/Device is connected (check with adb devices).
Install scrcpy (e.g., brew install scrcpy on macOS, or download binaries for Windows/Linux).
Execution Setup:
Start the Mobile Mirroring: Open a new terminal and run scrcpy to mirror your Android screen. This window will show the live automation.
code
Bash
scrcpy
Start the Mobile Next Agent: Open the Gemini CLI in a separate terminal.
code
Bash
gemini
4. Execute the Test with a Single Prompt
Inside the Gemini CLI, enter the following prompt for the Shopee test case. Watch the scrcpy window as the AI executes the steps!
code
Bash
@mobile-mcp Open the Shopee application. Search for a product named "TWS Headset Bluetooth 5.0". From the search results, tap on the first product listing. Select the color "Black" (if available), then add the item to the shopping cart. Go to the shopping cart, tap the "Checkout" button, and then verify that the screen displays the final "Payment Method" selection screen.
🌟 Project Showcase: AI Mobile E-commerce Automation
Badge	Status
Agent	
![alt text](https://img.shields.io/badge/Orchestrator-Gemini%20CLI-blue)
Tool	
![alt text](https://img.shields.io/badge/Mobile%20Tool-Mobile%20Next%20MCP-9C27B0)
Visualization	
![alt text](https://img.shields.io/badge/Visualization-scrcpy-brightgreen)
Target	Mobile (Android/iOS)
🎯 Overview
This project highlights a cutting-edge approach to mobile QA where a Large Language Model (LLM) acts as the quality assurance engineer. By bridging the Gemini CLI (the decision-making AI) with the Mobile Next MCP (the device interaction tool), we achieve high-fidelity, natural language-driven mobile test automation. The use of scrcpy ensures the process is visually clear, making it perfect for live demos and portfolio presentations.
🧪 Test Scenario: Shopee Product Checkout & Validation
The scenario simulates a typical user purchasing a product on the native Shopee application.
Step	Action	Description
1	Launch App	Open the native Shopee application.
2	Search	Use the search bar to find an item (e.g., "TWS Headset Bluetooth 5.0").
3	Select Product	Click the first search result to view details.
4	Configure & Add to Cart	Select an option (e.g., "Black" color) and confirm adding to the cart.
5	Initiate Checkout	Navigate to the cart and start the checkout process.
6	Verification	Assert that the application successfully navigated to the final "Payment Method" screen, validating the entire funnel is operational.
🔑 Key Component: Visualizing with scrcpy
scrcpy is used to stream the device screen to the desktop in real-time. This provides an immediate and clear visual confirmation that the AI agent's commands are being executed correctly on the device, demonstrating the practical application of the Mobile Next MCP's tools like mobile_tap and mobile_type.



