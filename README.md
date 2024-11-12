# Alejandro Scandroli's Alfred Workflows Collection

A collection of workflows that I have created to enhance my productivity. Each workflow is crafted with a focus on simplicity, composability, and _tailorability_.

> [!IMPORTANT]
> This is a work in progress. I'm still trying to recover and organize all my workflows.

## 📜 Guiding Principles

1. **Keyboard-First Approach**

   * The workflows are designed to keep your hands on the keyboard.

2. **Keyword-Based Search**

   * Inspired by JetBrains’s “Double Shift” Search Everywhere feature, I prioritize keyword-based searching in my workflows. Instead of relying on remembering specific shortcuts, you can simply type keywords related to the functionality you want to execute. This approach makes it easier to access the tools and commands you need without the mental load of memorizing multiple key combinations.

3. **No Additional Dependencies**

   * All scripts used in these workflows are written in Bash or Swift, which are natively supported on macOS.
   * Bash scripts make extensive use of JQ for seamless integration with existing CLI tools.
   * Swift scripts are kept as single-file scripts whenever possible.

4. **Script Filter JSON Format**

   * Instead of implementing fuzzy search, filtering and ordering I make extensive use of Alfred’s script filter and its JSON format. Script filters make workflows highly customizable and easy to maintain. Some of my workflows are as simple as a JSON file containing Alfred’s Script Filter JSON format.

5. **Customization**

   * Each workflow is designed with simplicity and the **expectation** that users will extend and adapt it to fit their specific needs and applications. 
   * Each workflow includes the original, modifiable scripts rather than compiled binaries, allowing users to tailor and extend them as needed.

6. **Interaction with Running Applications**

    * The main goal of the workflows is to save time when interacting with applications. The methods for interaction are:
        * NS Apple Script when the application is scriptable and has `NSAppleScriptEnabled`.
        * UIElementInspector for applications using the Cocoa UI framework and APIs.
        * Custom URL Schemes: Using custom URL schemes to trigger specific actions within applications that support them (eg: Rectangle)
        * Command Line Arguments: Directly interacting with CLI applications and adapting the output to the Script Filter JSON format.
        * Accessibility API: For non-Cocoa applications that still provide proper accessibility labels and attributes, allowing workflows to interact with their UI elements.
        * Shortcuts: for applications by **lazy** developers where none of the previous methods work (e.g., Electron-based applications). The workflow will trigger the key combination for a specific shortcut.

## 💡 Inspiration

The design and functionality of these workflows are inspired by some of the best tools and features that emphasize simplicity and power in productivity software:

* Humanized’s Enso Launcher: Inspired by its command-centric interface and the way it empowers users to perform tasks quickly without leaving the keyboard.
* JetBrains’s “Double Shift” Search Everywhere Feature: Borrowed the idea of a universal, context-aware search function that allows quick access to anything within reach, enhancing the searchability and efficiency within Alfred.
* Augment Text’s Liquids App: Influenced by its focus on text manipulation and ease of access to powerful text-editing functions.

These tools have shaped my approach and have conditioned the way I look at software.

## 🛠️ Workflows

|                                                                              |                  Implementation                  | Status                  | Comments |
|------------------------------------------------------------------------------|:------------------------------------------------:|-------------------------| ------ |
| [**AWS Console**](https://github.com/ascandroli/alfred-aws-console-workflow) |             Script Filter JSON file              | production but outdated | still usable |
| [**Menu Dump**](https://github.com/ascandroli/menudump)                                                                |             Cocoa UIElementInspector             | production but legacy   | I'll port it to swift |
| **Play / Pause**                                                             |                     Shortcut                     | production ready        |
| **Rectangle**                                                                | Script Filter JSON file & Scriptable Application | production ready        |
| **Shift+Shift**                                                              |       Script Filter JSON file & Shortcuts        | production ready        |
| **Toggle Case**                                                              |                      Swift                       | production ready        |
| **YKman**                                                                    |             CLI wrapper (bash + jq)              | production ready        |
| **Vault**                                                                    |             CLI wrapper (bash + jq)              | in development          |
| **Liquid Clone**                                                             |             Universal (Text) Actions             | experimental            |
| **.sdef Reader**                                                             |           meta Scriptable Application            | experimental            |
| **Now Do This**                                                              |                       bash                       | ultra experimental      | Inspired by Notational Velocity |
| **xbar**                                                                     |           meta CLI wrapper (bash + jq)           | abandoned               |                                         

For detailed instructions on how to use each workflow, refer to the individual workflow folders or files.
