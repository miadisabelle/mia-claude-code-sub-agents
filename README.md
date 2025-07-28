# Claude Code Subagents Collection

A comprehensive collection of 32 specialized AI subagents for [Claude Code](https://docs.anthropic.com/en/docs/claude-code), designed to enhance development workflows with domain-specific expertise and intelligent automation.

## 🚀 Overview

This repository contains a curated set of specialized subagents that extend Claude Code's capabilities across the entire software development lifecycle. Each subagent is an expert in a specific domain, automatically invoked based on context analysis or explicitly called when specialized expertise is needed.

### Key Features
- **🤖 Intelligent Auto-Delegation**: Claude Code automatically selects optimal agents based on task context
- **🔧 Domain Expertise**: Each agent specializes in specific technologies, patterns, and best practices
- **🔄 Multi-Agent Orchestration**: Seamless coordination between agents for complex workflows
- **📊 Quality Assurance**: Built-in review and validation patterns across all domains
- **⚡ Performance Optimized**: Agents designed for efficient task completion and resource utilization

## Available Subagents

### 🏗️ Development & Architecture
- **[backend-architect](backend-architect.md)** - Design RESTful APIs, microservice boundaries, and database schemas
- **[frontend-developer](frontend-developer.md)** - Build React components, implement responsive layouts, and handle client-side state management
- **[mobile-developer](mobile-developer.md)** - Develop React Native or Flutter apps with native integrations
- **[graphql-architect](graphql-architect.md)** - Design GraphQL schemas, resolvers, and federation patterns
- **[architect-reviewer](architect-review.md)** - Reviews code changes for architectural consistency and design patterns

### 💻 Language & Framework Specialists
- **[python-pro](python-pro.md)** - Write idiomatic Python code with advanced features and optimizations
- **[golang-pro](golang-pro.md)** - Write idiomatic Go code with goroutines, channels, and interfaces
- **[typescript-pro](typescript-pro.md)** - Advanced TypeScript development with type safety and modern patterns
- **[react-pro](react-pro.md)** - Expert React development with hooks, performance optimization, and best practices
- **[nextjs-pro](nextjs-pro.md)** - Next.js specialist for SSR, SSG, and full-stack React applications
- **[postgres-pro](postgres-pro.md)** - PostgreSQL database expert for advanced queries and optimizations
- **[electron-pro](electorn-pro.md)** - Electron desktop application development and cross-platform solutions

### ☁️ Infrastructure & Operations
- **[devops-incident-responder](devops-incident-responder.md)** - Debug production issues, analyze logs, and fix deployment failures
- **[deployment-engineer](deployment-engineer.md)** - Configure CI/CD pipelines, Docker containers, and cloud deployments
- **[cloud-architect](cloud-architect.md)** - Design AWS/Azure/GCP infrastructure and optimize cloud costs
- **[database-optimizer](database-optimizer.md)** - Optimize SQL queries, design efficient indexes, and handle database migrations
- **[incident-responder](incident-responder.md)** - Handles production incidents with urgency and precision
- **[dx-optimizer](dx-optimizer.md)** - Developer Experience specialist that improves tooling, setup, and workflows

### 🔍 Quality & Security
- **[code-reviewer](code-reviewer.md)** - Expert code review for quality, security, and maintainability
- **[security-auditor](security-auditor.md)** - Review code for vulnerabilities and ensure OWASP compliance
- **[test-automator](test-automator.md)** - Create comprehensive test suites with unit, integration, and e2e tests
- **[performance-engineer](performance-engineer.md)** - Profile applications, optimize bottlenecks, and implement caching strategies
- **[debugger](debugger.md)** - Debugging specialist for errors, test failures, and unexpected behavior

### 📊 Data & AI
- **[data-scientist](data-scientist.md)** - Data analysis expert for SQL queries, BigQuery operations, and data insights
- **[data-engineer](data-engineer.md)** - Build ETL pipelines, data warehouses, and streaming architectures
- **[ai-engineer](ai-engineer.md)** - Build LLM applications, RAG systems, and prompt pipelines
- **[ml-engineer](ml-engineer.md)** - Implement ML pipelines, model serving, and feature engineering
- **[prompt-engineer](prompt-engineer.md)** - Optimizes prompts for LLMs and AI systems

### 🎯 Specialized Domains
- **[api-documenter](api-documenter.md)** - Create OpenAPI/Swagger specs and write developer documentation
- **[documentation-expert](documentation-expert.md)** - Professional technical writing and comprehensive documentation systems
- **[payment-integration](payment-integration.md)** - Integrate Stripe, PayPal, and payment processors
- **[quant-analyst](quant-analyst.md)** - Build financial models, backtest trading strategies, and analyze market data
- **[legacy-modernizer](legacy-modernizer.md)** - Refactor legacy codebases and implement gradual modernization
- **[context-manager](context-manager.md)** - Manages context across multiple agents and long-running tasks

## 📦 Installation

### Quick Setup
These subagents are automatically available when placed in the `~/.claude/agents/` directory. Claude Code will automatically detect and load them on startup.

```bash
# Clone the repository to your Claude agents directory
cd ~/.claude
git clone https://github.com/wshobson/agents.git

# Or if the directory already exists, pull the latest updates
cd ~/.claude/agents
git pull origin main
```

### Manual Installation
Alternatively, you can manually copy individual agent files:

```bash
# Copy specific agents to your Claude agents directory
cp /path/to/agents/*.md ~/.claude/agents/
```

### Verification
To verify agents are loaded correctly:

```bash
# List all available agents
ls ~/.claude/agents/*.md

# Check Claude Code recognizes the agents (run in Claude Code)
# "List all available subagents"
```

## 🔧 Usage

### Automatic Invocation (Recommended)
Claude Code intelligently analyzes your request and automatically delegates to the most appropriate subagent(s) based on:
- **Context Analysis**: Keywords, file types, and project structure
- **Task Classification**: Development, debugging, optimization, etc.
- **Domain Expertise**: Matching requirements to specialist knowledge
- **Workflow Patterns**: Common multi-agent coordination scenarios

**Example**: `"Implement user authentication with secure password handling"` → Automatically uses: `backend-architect` → `security-auditor` → `test-automator`

### Explicit Invocation
For specific expertise or when you want control over agent selection:

```bash
# Direct agent requests
"Use the code-reviewer to check my recent changes"
"Have the security-auditor scan for vulnerabilities"
"Get the performance-engineer to optimize this bottleneck"

# Multi-agent requests
"Have backend-architect design the API, then security-auditor review it"
"Use data-scientist to analyze this dataset, then ai-engineer to build recommendations"
```

### Hybrid Approach
Combine automatic and explicit invocation:

```bash
# Start explicit, let Claude coordinate the rest
"Use backend-architect to design a REST API for user management, then handle the implementation automatically"

# Explicit validation after automatic work
"Implement this feature automatically, then have security-auditor review the result"
```

## 💡 Usage Examples

### Single Agent Tasks

#### 🔍 Code Quality & Review
```bash
"Use code-reviewer to analyze this component for best practices"
"Have security-auditor check for OWASP compliance issues"
"Get test-automator to create comprehensive test coverage"
```

#### 🏗️ Development Tasks  
```bash
"Get backend-architect to design a user authentication API"
"Use frontend-developer to create a responsive dashboard layout"
"Have mobile-developer build iOS/Android login screens"
```

#### ☁️ Infrastructure & Operations
```bash
"Have devops-incident-responder analyze these production logs"
"Use cloud-architect to design a scalable AWS architecture"
"Get deployment-engineer to set up CI/CD pipeline"
```

#### 📊 Data & AI
```bash
"Get data-scientist to analyze this customer behavior dataset"
"Use ai-engineer to build a RAG system for document search"
"Have ml-engineer create a recommendation engine"
```

### Multi-Agent Workflows

#### 🚀 Feature Development Workflow
```bash
"Implement user authentication feature"
# Automatically coordinates: backend-architect → frontend-developer → test-automator → security-auditor
```

#### ⚡ Performance Optimization Workflow  
```bash
"Optimize the checkout process performance"
# Automatically coordinates: performance-engineer → database-optimizer → frontend-developer
```

#### 🚨 Production Incident Workflow
```bash
"Debug high memory usage in production"
# Automatically coordinates: incident-responder → devops-incident-responder → performance-engineer
```

#### 🔄 Code Modernization Workflow
```bash
"Modernize this legacy Python application"
# Automatically coordinates: legacy-modernizer → python-pro → test-automator → code-reviewer
```

## 📋 Subagent Format

Each subagent follows a standardized structure for consistent behavior and optimal integration:

### File Structure
```markdown
---
name: subagent-name
description: When this subagent should be invoked
tools: tool1, tool2  # Optional - defaults to all tools
---

# Subagent Name

**Role**: Detailed role description and primary responsibilities

**Expertise**: Specific technologies, frameworks, and domain knowledge

**Key Capabilities**:
- Capability 1: Description
- Capability 2: Description
- Capability 3: Description

System prompt defining the subagent's specialized behavior, decision-making patterns, and interaction style with other agents.
```

### Required Components
- **Name**: Kebab-case filename matching the agent name
- **Description**: Clear trigger conditions for automatic invocation
- **Role Definition**: Specific responsibilities and boundaries
- **Expertise Areas**: Technologies, patterns, and domain knowledge
- **System Prompt**: Detailed instructions for specialized behavior

### Optional Components
- **Tools**: Specific Claude Code tools (defaults to all available tools)
- **Dependencies**: Other agents this one commonly works with
- **Patterns**: Common workflow patterns and coordination scenarios

## 🔄 Agent Orchestration Patterns

Claude Code automatically coordinates agents using intelligent patterns based on task complexity and requirements:

### 🔗 Sequential Workflows
**Pattern**: `User Request → Agent A → Agent B → Agent C → Result`

**Use Cases**: Feature development, step-by-step processes, dependent tasks
```bash
Example: "Build a new API feature"
backend-architect → frontend-developer → test-automator → security-auditor
```

**Benefits**: 
- Ensures proper dependencies and order
- Each agent builds on previous agent's work
- Quality gates at each step

### ⚡ Parallel Execution
**Pattern**: `User Request → Agent A + Agent B (simultaneously) → Merge Results`

**Use Cases**: Independent analysis, optimization tasks, research
```bash
Example: "Optimize application performance" 
performance-engineer + database-optimizer → Combined recommendations
```

**Benefits**:
- Faster execution for independent tasks
- Multiple perspectives on complex problems
- Comprehensive analysis coverage

### 🎯 Conditional Branching
**Pattern**: `User Request → Analysis → Route to appropriate specialist`

**Use Cases**: Debugging, problem diagnosis, context-dependent solutions
```bash
Example: "Fix this bug"
debugger (analyzes) → Routes to: backend-architect OR frontend-developer OR devops-incident-responder
```

**Benefits**:
- Intelligent routing based on context analysis
- Avoids unnecessary agent involvement
- Specialized expertise for specific problems

### ✅ Review & Validation
**Pattern**: `Primary Agent → Review Agent → Final Result`

**Use Cases**: Security validation, code review, quality assurance
```bash
Example: "Implement payment processing"
payment-integration → security-auditor → Validated implementation
```

**Benefits**:
- Built-in quality assurance
- Expert validation of critical components
- Risk mitigation for sensitive operations

### 🔄 Iterative Refinement
**Pattern**: `Agent A → Review → Agent A (refined) → Final Result`

**Use Cases**: Optimization, improvement, iterative development
```bash
Example: "Improve code quality"
code-reviewer → performance-engineer → code-reviewer → Optimized code
```

**Benefits**:
- Progressive improvement
- Multiple optimization passes
- Convergence on optimal solutions

## 🎯 When to Use Which Agent

### 🏗️ Planning & Architecture
| Agent | Best For | Example Use Cases |
|-------|----------|-------------------|
| **backend-architect** | API design, system architecture | RESTful APIs, microservices, database schemas |
| **frontend-developer** | UI/UX planning, component design | React components, responsive layouts, state management |
| **cloud-architect** | Infrastructure design, scalability | AWS/Azure/GCP architecture, cost optimization |
| **graphql-architect** | GraphQL system design | Schema design, resolvers, federation |

### 💻 Implementation & Development  
| Agent | Best For | Example Use Cases |
|-------|----------|-------------------|
| **python-pro** | Python development | Django/FastAPI apps, data processing, async programming |
| **golang-pro** | Go development | Microservices, concurrent systems, CLI tools |
| **typescript-pro** | TypeScript development | Type-safe applications, advanced TS features |
| **react-pro** | React expertise | Hooks, performance optimization, advanced patterns |
| **nextjs-pro** | Next.js applications | SSR/SSG, full-stack React, routing |

### ☁️ Operations & Maintenance
| Agent | Best For | Example Use Cases |
|-------|----------|-------------------|
| **devops-incident-responder** | Production issues, deployments | Log analysis, deployment failures, system debugging |
| **incident-responder** | Critical outages | Immediate response, crisis management, escalation |
| **deployment-engineer** | CI/CD, containerization | Docker, Kubernetes, pipeline configuration |
| **database-optimizer** | Database performance | Query optimization, indexing, migration strategies |

### 📊 Analysis & Optimization
| Agent | Best For | Example Use Cases |
|-------|----------|-------------------|
| **performance-engineer** | Application performance | Bottleneck analysis, caching strategies, optimization |
| **security-auditor** | Security assessment | Vulnerability scanning, OWASP compliance, threat modeling |
| **data-scientist** | Data analysis | SQL queries, BigQuery, insights and reporting |
| **code-reviewer** | Code quality | Best practices, maintainability, architectural review |

### 🧪 Quality Assurance
| Agent | Best For | Example Use Cases |
|-------|----------|-------------------|
| **test-automator** | Testing strategy | Unit tests, integration tests, E2E test suites |
| **debugger** | Bug investigation | Error analysis, test failures, troubleshooting |
| **architect-reviewer** | Design validation | Architectural consistency, pattern compliance |

## 📚 Best Practices

### 🎯 Task Delegation Strategy
1. **Trust Automatic Delegation** - Claude Code's intelligence excels at context analysis and optimal agent selection
2. **Provide Rich Context** - Include tech stack, constraints, quality requirements, and project background
3. **Start High-Level** - Begin with business objectives and let agents break down technical implementation
4. **Leverage Agent Expertise** - Each agent is fine-tuned for their specific domain and decision patterns

### 🔄 Multi-Agent Workflow Optimization
5. **Enable Agent Coordination** - Let agents naturally collaborate rather than micromanaging the sequence
6. **Validate Integration Points** - Review how different agents' outputs combine and interact
7. **Provide Cross-Agent Context** - Ensure agents have necessary background from previous steps
8. **Monitor Workflow Efficiency** - Identify patterns that work well for your project types

### 🎛️ Strategic Explicit Control
9. **Use Explicit Invocation Purposefully** - When you need specific expertise or want to override automatic selection
10. **Design Review Chains** - Structure validation patterns like "architect → implement → security-review"
11. **Combine Complementary Specialists** - Use agents with different perspectives to validate each other's work
12. **Request Specific Analysis Depth** - Specify when you need surface-level vs. deep architectural analysis

### 📈 Performance & Quality Optimization
13. **Learn from Agent Patterns** - Observe which agent combinations work best for your use cases
14. **Iterate on Complex Requirements** - Use agent feedback to refine and clarify requirements
15. **Match Task Complexity** - Don't over-engineer simple tasks or under-resource complex ones
16. **Establish Quality Gates** - Build review and validation into your standard workflows

### 🧠 Advanced Usage Patterns
17. **Use Context-Manager** - For long-running projects spanning multiple sessions
18. **Leverage Documentation-Expert** - For maintaining project knowledge and onboarding
19. **Implement Continuous Review** - Have code-reviewer and security-auditor as regular validation steps
20. **Plan for Scalability** - Include cloud-architect and performance-engineer early in architecture decisions

## 🤝 Contributing

### Adding New Agents

To contribute a new subagent to the collection:

1. **Follow Naming Convention**
   - Use lowercase, hyphen-separated names (e.g., `backend-architect.md`)
   - Name should clearly indicate the agent's domain and role

2. **Use Standard Format**
   - Include proper frontmatter with `name`, `description`, and optional `tools`
   - Follow the structured format outlined in the [Subagent Format](#-subagent-format) section

3. **Write Clear Descriptions**
   - Description should clearly indicate when the agent should be automatically invoked
   - Include specific keywords and contexts that trigger the agent

4. **Define Specialized Behavior**
   - Include detailed system prompt with role, expertise, and capabilities
   - Define interaction patterns with other agents
   - Specify decision-making frameworks and priorities

5. **Test Integration**
   - Verify the agent can be automatically invoked based on description
   - Test explicit invocation with clear requests
   - Ensure compatibility with existing agent coordination patterns

### Quality Standards

- **Domain Expertise**: Agents should demonstrate deep knowledge in their specialization
- **Clear Boundaries**: Define what the agent does and doesn't handle
- **Integration Ready**: Design for seamless coordination with other agents
- **Consistent Voice**: Maintain professional, helpful, and expert tone

### Submission Process

1. Create the agent file following all standards
2. Test the agent with various invocation patterns
3. Submit a pull request with example use cases
4. Include documentation of the agent's unique value and integration patterns

## 🛠️ Troubleshooting

### Common Issues & Solutions

#### 🤖 Agent Selection Issues

**Problem**: Agent not being invoked automatically
- **Solution**: Use domain-specific keywords (e.g., "performance issue" → performance-engineer)
- **Solution**: Be explicit about task type (e.g., "review code" → code-reviewer)
- **Solution**: Include relevant file extensions or technology names

**Problem**: Unexpected agent selection
- **Solution**: Provide more context about tech stack and project requirements
- **Solution**: Use explicit invocation: "Use specific-agent to handle this task"
- **Solution**: Add project context in your request

#### 🔄 Multi-Agent Coordination

**Problem**: Multiple agents producing conflicting advice
- **Expected**: Different specialists may have different priorities (security vs. performance)
- **Solution**: Request reconciliation: "Reconcile recommendations from security-auditor and performance-engineer"
- **Solution**: Ask for prioritized recommendations based on your project constraints

**Problem**: Agents seem disconnected or lack context
- **Solution**: Provide comprehensive background in your request
- **Solution**: Reference previous conversations: "Building on the API design from backend-architect..."
- **Solution**: Use context-manager for long-running projects

#### ⚡ Performance & Quality

**Problem**: Agent responses too generic or surface-level
- **Solution**: Request specific depth: "Provide detailed analysis with code examples"
- **Solution**: Include specific constraints and requirements
- **Solution**: Ask for expert-level recommendations

**Problem**: Workflows taking too long or inefficient routing
- **Solution**: Use more specific language to trigger optimal agents directly
- **Solution**: Break complex requests into focused sub-tasks
- **Solution**: Leverage parallel execution patterns for independent tasks

### Getting Help & Support

#### Self-Service Debugging
1. **Review Agent Descriptions**: Check individual agent files for trigger conditions and capabilities
2. **Test Explicit Invocation**: Use direct agent calls to verify functionality
3. **Analyze Request Language**: Use more specific, domain-focused language
4. **Provide Rich Context**: Include project background, tech stack, and constraints

#### Advanced Troubleshooting
- **Enable Verbose Mode**: Request detailed explanations of agent selection rationale
- **Test Individual Agents**: Isolate issues by testing agents independently
- **Review Workflow Patterns**: Ensure your use case matches expected orchestration patterns
- **Check Agent Compatibility**: Verify agents work well together for your specific domain

#### When to Seek Help
- Persistent agent selection issues despite following guidelines
- Unexpected behavior that affects project outcomes
- Need for custom agent development or specialized domain coverage
- Complex multi-agent workflows requiring optimization

## 📖 Learn More

### Official Documentation
- **[Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code)** - Complete guide to Claude Code features and capabilities
- **[Subagents Documentation](https://docs.anthropic.com/en/docs/claude-code/sub-agents)** - Official subagent system documentation
- **[Claude Code GitHub](https://github.com/anthropics/claude-code)** - Source code and community contributions

### Advanced Topics
- **Multi-Agent Orchestration**: Understanding how agents coordinate and collaborate
- **Custom Agent Development**: Creating specialized agents for your domain
- **Workflow Optimization**: Designing efficient multi-agent workflows
- **Context Management**: Maintaining state across long-running projects

### Community Resources
- **Agent Examples**: Real-world use cases and implementation patterns
- **Best Practices Guide**: Community-driven recommendations for optimal usage
- **Integration Patterns**: Common workflows and coordination strategies
- **Performance Optimization**: Tips for efficient agent utilization

---

## 📊 Quick Reference

### Most Commonly Used Agents
1. **code-reviewer** - Quality assurance and best practices
2. **backend-architect** - API and system design
3. **frontend-developer** - UI/UX implementation
4. **security-auditor** - Security validation and compliance
5. **performance-engineer** - Optimization and bottleneck analysis

### Essential Coordination Patterns
- **Development**: `architect → implement → test → review`
- **Debugging**: `debugger → specialist → validator`
- **Optimization**: `performance-engineer + database-optimizer → validation`
- **Security**: `primary-agent → security-auditor → approval`

### Key Success Factors
- ✅ Trust automatic delegation for optimal results
- ✅ Provide rich context and specific requirements
- ✅ Use explicit invocation strategically
- ✅ Establish quality gates and validation patterns
- ✅ Learn from agent coordination patterns

*Happy coding with your AI specialist team! 🚀*