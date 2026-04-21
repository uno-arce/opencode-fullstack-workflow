**Opencode** is an open-source AI Agent for AI-assisted development. It comes with three available platforms such as: terminal-based interface, desktop application, or IDE extension. In this workflow, I used the opencode CLI by running it in WSL (Window subsystem for Linux).

## Components
1. **Opencode.JSON** - Global configuration for all opencode projects  
```
schema                       ## Set to default opencode schema url  
autoupdate                   ## Set to true for receiving recent updates
permissions                  
  ├── external directory     ## Allowed to see documents
  ├── read                   ## Deny to read sensitive keys
mcp                          ## Added google stitch mcp to read and get project context
agent                        ## Set three main agents each with respective subagents
  ├── build
  ├── plan
  ├── test                      
```
2. **Agents** - A collection of subagents with different expertise
```
code-architect               ## Reviews code and plans for best solutions
code-operator                ## Builds workflow automation and optimizations
schema-architect             ## Creates a type-safe schema based on requirements
ui-designer                  ## Generates a design and exports them as react components
code-tester                  ## Performs unit tests for user scenarios and features
e2e-tester                   ## Writes and tests scripts to simulate user behavior on both stacks
```
3. **Skills** - A collection of skills to teach agents/subagents
```
design-md                    ## A google stitch skill for creating DESIGN.md containing project design context
react-components             ## A google stitch skill for converting screens to a react component system
```

## Workflow Automation
This workflow shows the use of google stitch and google studio to generate frontend design and code, and opencode in utilizing the mcp server and subagents in creating a full stack scaffold and application features. 
<img width="1232" height="713" alt="image" src="https://github.com/user-attachments/assets/d966ef42-a5bb-4a9f-a6f2-20afc480c5a6" />
