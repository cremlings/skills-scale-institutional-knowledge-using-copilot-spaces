---
name: "Add Content to Project Management Process Docs"
description: "Request to add new content or updates to an existing program management process document."
title: "[Process Doc Update]: Create README for OctoAcme Project Management Docs with process summary and links"
labels: ["documentation", "process improvement"]
body:
  - type: dropdown
    id: process_doc
    attributes:
      label: "Which process document do you want to update?"
      description: "Select the program management process document you want to add content to. If this is a new process doc, choose ''."
      options:
        - "<new document>"
    validations:
      required: true

  - type: textarea
    id: content_summary
    attributes:
      label: "Summary of New Content"
      description: "Briefly describe the new content or update you want to add."
      value: |
        Create a comprehensive README for the `docs/` folder that serves as a central navigation hub for OctoAcme's project management processes:
        
        1. **Brief Summary of OctoAcme PM Processes** - Overview of core principles (Customer-first, Iterative delivery, Clear ownership, Data-informed decisions, Psychological safety)
        2. **Project Lifecycle Overview** - Visual representation of the five phases: Initiation → Planning → Execution → Release → Retrospective
        3. **Links to All Process Guides** - Organized by lifecycle phase with descriptions:
           - Project Initiation Guide
           - Project Planning
           - Execution & Tracking Guide
           - Release & Deployment Guide
           - Retrospective & Continuous Improvement
        4. **Cross-Cutting Guidance** - Risk Management & Communication, Roles & Personas, Project Management Overview
        5. **Key Artifacts Reference** - Table of deliverables throughout project lifecycle
        6. **Communication Cadence** - Standard meeting rhythms
        7. **Quick-Start Guide** - Navigation for different user types
        8. **Contributing Guidelines** - Link to process doc update template
    validations:
      required: true

  - type: textarea
    id: rationale
    attributes:
      label: "Why is this update needed?"
      description: "Explain the reason for this addition."
      value: |
        - **Gap Identified**: The `docs/` folder contains valuable, detailed process documentation but lacks a central entry point and navigation guide
        - **Improved Onboarding**: New team members need a clear, organized overview of OctoAcme's methodology and how to navigate the different phase-specific guides
        - **Better Discoverability**: A README makes it easier for anyone to understand which guide applies to their current project phase and role
        - **Centralized Knowledge**: This consolidates institutional knowledge into a single, searchable hub that makes OctoAcme's approach explicit and accessible
        - **Easy Updates**: The README references all process guides and makes it easy to identify what's available
    validations:
      required: true

  - type: textarea
    id: example_content
    attributes:
      label: "Suggested Content (optional)"
      description: "Paste the proposed new text, checklist, diagram, or example content you'd like to add. (Optional)"
      value: |
        A new `docs/README.md` file that includes:
        - Clear overview section explaining OctoAcme's five core principles and customer-first approach
        - Project lifecycle diagram showing the five phases and how they connect
        - Organized index of all process guides grouped by lifecycle phase with brief descriptions
        - Cross-cutting guidance section (Risk Management, Roles, Overview)
        - Key artifacts reference table showing what's created at each phase
        - Communication cadence overview with meeting frequencies
        - Quick-start guide for getting started with a new project
        - Contributing guidelines with link to the process doc update issue template

  - type: checkboxes
    id: acceptance_criteria
    attributes:
      label: "Acceptance Criteria"
      description: "Check all that apply:"
      options:
        - label: "Content aligns with existing process docs"
          required: true
        - label: "Update improves clarity or closes a documented gap"
          required: true
        - label: "Proposed content has been reviewed with stakeholders (if needed)"
          required: true
