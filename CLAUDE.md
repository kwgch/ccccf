# Claude Code Configuration

## Quick Check
```bash
# Is Claude-Flow available in this project?
if [ -f "./claude-flow" ] || command -v claude-flow &> /dev/null; then
    echo "✅ Claude-Flow is available"
else
    echo "❌ Claude-Flow not found - using standard tools"
fi
```

## TL;DR
- **Claude-Flow may be available** - Check with `ls ./claude-flow` or `which claude-flow`
- **For simple tasks**: Always use standard Edit, Write, Bash tools
- **For complex tasks**: If claude-flow is available, consider it for parallel work
- **Not installed?**: That's fine - continue with standard development approach

## Overview
This project MAY have Claude-Flow installed. If available, it's a powerful tool for:
- Parallel execution of multiple independent tasks
- Persistent memory across sessions
- Systematic development with SPARC methodology
- Multi-agent coordination for large projects

**First, check if Claude-Flow is available:**
```bash
# Check for local executable
ls -la ./claude-flow

# Or check global installation
which claude-flow

# If not found, continue with standard development
```

## When to Use Claude-Flow

### Use Claude-Flow for:
1. **Large Feature Development**: Breaking down complex features into parallel tasks
2. **Multi-Component Changes**: When changes span backend, frontend, and database
3. **Research-Heavy Tasks**: Utilizing memory to store findings and decisions
4. **Team Simulation**: Running multiple specialized agents (architect, developer, tester)

### Continue Using Standard Tools for:
1. **Simple File Edits**: Direct edits with Edit/Write tools
2. **Quick Fixes**: Small bug fixes or typo corrections
3. **Single-File Operations**: When working within one file or component
4. **Direct Commands**: Running simple bash commands or tests

## Quick Reference

### If Claude-Flow IS Available
```bash
# Check if Claude-Flow is working
./claude-flow status

# Store important information for later
./claude-flow memory store <key> "<value>" --namespace <category>

# Query stored information
./claude-flow memory query "<search-term>"

# Use SPARC for complex development
./claude-flow sparc "<task-description>"

# List available SPARC modes
./claude-flow sparc modes
```

### If Claude-Flow is NOT Available
Continue with standard Claude Code approach:
- Use the Task tool for complex multi-step operations
- Store important information in comments or documentation
- Break down complex tasks into manageable pieces
- Use standard tools effectively

### Standard Development Commands
```bash
# Project-specific build commands
npm run build
npm run test
npm run lint
npm run dev
```

## Claude-Flow Usage Examples (If Available)

### Example 1: Parallel Development
When you need to implement multiple independent components:
```bash
# WITH Claude-Flow: Use memory to coordinate
./claude-flow memory store current_task "implementing auth system"

# WITHOUT Claude-Flow: Use the Task tool directly
# The Task tool can still run parallel operations
```

### Example 2: Memory-Driven Development
When working on long-running projects with multiple sessions:
```bash
# Store architectural decisions
./claude-flow memory store architecture_decision "Using microservices pattern for scalability"

# Store API endpoints as you design them
./claude-flow memory store api_endpoints "GET /users, POST /users, PUT /users/:id"

# Later, query your decisions
./claude-flow memory query architecture
```

### Example 3: SPARC for Complex Features
When implementing a major feature with many moving parts:
```bash
# Use SPARC orchestrator for comprehensive development
./claude-flow sparc "implement real-time chat system with authentication"

# Or use specific modes for focused tasks
./claude-flow sparc run architect "design chat system architecture"
./claude-flow sparc run tdd "implement message queue"
```

## Available SPARC Modes (If Claude-Flow is Installed)

Use `./claude-flow sparc modes --verbose` to see detailed descriptions:
- **architect**: System design and architecture
- **code**: Clean code implementation
- **tdd**: Test-driven development
- **debug**: Debugging and troubleshooting
- **security-review**: Security analysis
- **docs-writer**: Documentation
- **integration**: System integration
- **devops**: Deployment and CI/CD
- **spec-pseudocode**: Requirements analysis
- **mcp**: External tool integration
- **sparc**: Orchestrator mode (default)
- And more specialized modes...

## Best Practices

### When Working with Claude-Flow
1. **Check Status First**: Always run `./claude-flow status` to verify it's available
2. **Use Memory Wisely**: Store only important decisions, not temporary values
3. **Namespace Organization**: Use clear namespaces (project, architecture, decisions, etc.)
4. **Parallel Tasks**: Use the Task tool for truly independent work only
5. **SPARC Selection**: Choose the right SPARC mode for your specific task

### General Development Principles
- Write clean, maintainable code
- Follow project conventions
- Test your changes
- Document complex logic
- Handle errors gracefully

## Memory System

### Common Memory Patterns
```bash
# Store key decisions
./claude-flow memory store decision_db "Using PostgreSQL for ACID compliance" --namespace architecture

# Track completed work
./claude-flow memory store completed_auth "JWT authentication implemented with refresh tokens" --namespace milestones

# Store configuration
./claude-flow memory store api_version "v2" --namespace config

# Query by namespace
./claude-flow memory query "" --namespace architecture
```

### Suggested Namespaces
- **architecture**: Design decisions and patterns
- **milestones**: Completed features and achievements
- **config**: Configuration values and settings
- **research**: Findings and external references
- **issues**: Known problems and their solutions

## Decision Framework

### Should I Use Claude-Flow?

**YES, use Claude-Flow when:**
- The task involves 3+ independent components
- You need to remember decisions across sessions
- The feature requires multiple specialized approaches (architecture + implementation + testing)
- You're starting a new major feature or system

**NO, stick to standard tools when:**
- Making quick fixes or small changes
- Working within a single file
- The task is straightforward and linear
- You just need to run some commands

## Claude-Flow Files

- **`./claude-flow`**: Local executable (use this instead of npx)
- **`.roomodes`**: SPARC mode configurations
- **`.roo/`**: SPARC templates and workflows
- **`memory/`**: Persistent storage location
- **`memory/claude-flow-data.json`**: Memory database

## Quick Decision Guide

```
Task: "Add a new button to the UI"
→ Use: Standard Edit/Write tools

Task: "Implement user authentication with JWT, sessions, and 2FA"
→ Use: Claude-Flow with parallel tasks or SPARC

Task: "Fix a typo in the README"
→ Use: Standard Edit tool

Task: "Build a real-time chat system with rooms, messages, and notifications"
→ Use: Claude-Flow SPARC orchestrator

Task: "Run tests and fix any failures"
→ Use: Standard Bash tool with npm test

Task: "Design and implement a microservices architecture"
→ Use: Claude-Flow with architect mode and memory storage
```

## Troubleshooting

### Claude-Flow Not Found?
```bash
# Check if it's installed locally
ls -la ./claude-flow

# Check global installation
which claude-flow || which npx

# Want to install it?
npx claude-flow@latest init --sparc

# Or continue without it - that's perfectly fine!
```

### Claude-Flow Exists but Not Working?
```bash
# Make it executable
chmod +x ./claude-flow

# Check memory system
./claude-flow memory stats

# Reinitialize if needed
npx claude-flow init --sparc
```

## Summary

Claude-Flow is a powerful OPTIONAL tool that MAY be available in this project for:
1. **Parallel task execution** - Run multiple independent tasks simultaneously
2. **Persistent memory** - Store and retrieve information across sessions
3. **SPARC methodology** - Systematic development with specialized AI modes
4. **Complex orchestration** - Coordinate large, multi-faceted projects

**Key Points:**
- Check if it's available first: `ls ./claude-flow`
- Use it when it adds value for complex tasks
- Not available? No problem - standard tools work great
- Don't feel obligated to use it for simple tasks

## Important Notes

- Claude-Flow is optional - use it when it helps, not because it's there
- The `./claude-flow` executable is faster than `npx claude-flow`
- Memory persists between sessions in `memory/claude-flow-data.json`
- You can always check available commands with `./claude-flow --help`
