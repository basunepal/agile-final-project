---
name: Item
about: Item Description
title: ''
labels: ''
assignees: ''

---

name: User Story
description: Describe a new feature or piece of functionality from a user's perspective.
title: "[STORY] As a <user>, I need <goal>, so that <reason>"
labels: ["enhancement"]
assignees: []

body:
  - type: markdown
    attributes:
      value: |
        # 📝 User Story & Acceptance Criteria
        *(Fill out the fields below to create a complete, ready-to-work-on User Story.)*

  - type: textarea
    id: user_story
    attributes:
      label: "User Story"
      description: "Use the standard User Story format (As a... I need... So that...)"
      placeholder: |
        As a [Role/Persona/User Type]
        I need to [Goal/Action]
        So that [Value/Reason]
    validations:
      required: true

  - type: textarea
    id: acceptance_criteria
    attributes:
      label: "Acceptance Criteria (Gherkin)"
      description: "Define the success conditions using Given... When... Then... syntax."
      placeholder: |
        GIVEN a certain context
        WHEN an action is performed
        THEN a verifiable outcome is achieved
    validations:
      required: true

  - type: dropdown
    id: story_estimate
    attributes:
      label: "Story Estimate (Story Points)"
      description: "Select the estimated effort from the Fibonacci sequence."
      options:
        - None
        - 1 Point
        - 2 Points
        - 3 Points
        - 5 Points
        - 8 Points
      default: 0
    validations:
      required: true

  - type: checkboxes
    id: invest_check
    attributes:
      label: "INVEST Criteria Check"
      description: "Check the qualities this story meets."
      options:
        - label: Independent
        - label: Negotiable
        - label: Valuable
        - label: Estimable
        - label: Small
        - label: Testable
