
# ShaderCells

ShaderCells provides resources for writing, debugging, and optimizing ReShadeFX (HLSL) shaders. This repository includes a specialized AI agent skill and a comprehensive Retrieval-Augmented Generation (RAG) knowledge base.

## Agent Skills (`./skills`)

Extend AI CLI tools with the **reshadefx-coder** skill. Agent skills provide specialized capabilities that allow AI models to execute code, search files, and perform complex tasks autonomously. Learn more at the [Anthropic Agent Skills](https://docs.anthropic.com/en/docs/build-with-claude/tool-use) site.

### Installation

Copy the `skills/reshadefx-coder` folder to your CLI's search path:

> Example: `./.agents/skills/reshadefx-coder`

**Gemini CLI**

- Global Path: `~/.gemini/skills/`
- Local Path: `./.agents/skills/`

**Claude Code**

- Global Path: `~/.claude/skills/`
- Local Path: `./.claude/skills/`

**Mistral Vibe**

- Global Path: `~/.vibe/skills/`
- Local Path: `./.vibe/skills/`

## Chatbot Experts (`./rag`)

Turn popular chatbot applications into ReShadeFX experts using the provided RAG files. Retrieval-Augmented Generation (RAG) connects AI models to specific data sources, ensuring responses are accurate and grounded in the provided technical documentation.

### 1. Download Resources

1. Download the repository as a `.zip` from the [Project Page](https://papadanku.github.io/ShaderCells/).
2. Unzip the files to a known location.

### 2. Configure Your Assistant

#### Google Gemini (Gems)

1. Open [Gemini](https://gemini.google.com/app) and log in.
2. Select **Gems** > **New Gem**.
3. Paste `rag/Description.txt` into **Description**.
4. Paste `rag/Instructions.txt` into **Instructions**.
5. Upload all files from `rag/knowledge/` to the **Knowledge** box.

#### Mistral AI (Le Chat)

1. Open [Le Chat](https://chat.mistral.ai/chat) and log in.
2. Open the **Intelligence** tab and select **Libraries**.
3. Click **New Library**, name it "Shader Knowledge," and upload all files from `rag/knowledge/`.
4. Open the **Agents** tab and select **Create an agent**.
5. Paste `rag/Description.txt` into **Purpose** and `rag/Instructions.txt` into **Instructions**.
6. Open the **Knowledge** tab and checkmark the "Shader Knowledge" library.

#### AnythingLLM (Local)

1. Open AnythingLLM and create a workspace named "ReShadeFX".
2. Click the **Upload** icon, add all files from `rag/knowledge/`, and select **Move to Workspace**.
3. Open **Chat Settings** > **System Prompt** and paste `rag/Instructions.txt`.

#### GPT4All (Local)

1. Open GPT4All and navigate to **Settings** > **LocalDocs**.
2. Add `rag/knowledge/` to the indexed folders.
3. In **Settings** > **Model**, clone your preferred model.
4. Paste `rag/Instructions.txt` into the **System Message** field.
