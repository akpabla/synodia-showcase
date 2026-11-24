# Case study: evolving a planning application into an agentic delivery platform

## The delivery problem

A conversational assistant can simplify planning interactions, but enterprise adoption also needs traceable evidence, clear permissions, recoverable execution and accountable decisions. Synodia's development therefore combines product functionality with platform controls.

## Scope and ownership

This is an ongoing product-development initiative, not a completed enterprise customer rollout. My contribution focuses on product requirements, prioritization, technical direction, review and acceptance, with AI assistance used during implementation. I do not present generated code as evidence of unaided authorship or imply a staffed delivery organization.

## Representative decisions

| Decision | Rationale | Trade-off / remaining validation |
|---|---|---|
| Preserve deterministic planning calculations | AI can explain scenarios while calculations remain testable | Agents must use tool outputs faithfully |
| Separate evidence review from execution approval | A reviewed requirement is not permission to change Jira | Adds explicit approval states and user-experience work |
| Separate ordinary imports from external writes | Reading authorized data should not create repetitive approval friction | Read access still needs identity and scope enforcement |
| Introduce durable workflows | Long operations must tolerate interruptions and human review | Recovery and cancellation require targeted acceptance tests |
| Start with bounded specialist collaboration | Explicit inputs and outputs make progress and failures easier to inspect | Complete agent integration remains in development |
| Keep providers replaceable | Customers may need different inference or deployment arrangements | Provider compatibility must be evaluated rather than assumed |

## Delivery sequence

1. Establish planning and connector foundations.
2. Add discovery, evidence retrieval and human review.
3. Strengthen governance, recovery and source access.
4. Extend PI execution and methodology-aware analytics.
5. Validate the regression baseline in an isolated environment.
6. Connect durable shared-agent runs, then Discovery → Requirements Readiness.
7. Expand collaboration and qualify the complete enterprise release.

This sequence is a development roadmap, not a claim that every stage is complete.

## A concrete regression lesson

Browser regression testing exposed two useful issues: saved source settings could disappear from the desktop view, and capacity editing could create competing proposals. The response was to isolate tests from the developer workspace, correct the settings filter, combine related matrix changes into one proposal and update tests to follow the approval lifecycle.

The project-management lesson is that governance must be tested as a user journey. A control can be technically present while still creating confusing handoffs or repeated work.

## Success criteria

- A user can follow a recommendation to its supporting evidence.
- Unsupported claims and missing requirements remain visible.
- Planning explanations match calculated results.
- Unauthorized users cannot retrieve restricted evidence or execute changes.
- Interrupted operations recover without duplicate external actions.
- Users can distinguish a draft, a human-reviewed artifact and an approved write.

## Open risks

Model grounding, source-permission coverage, live integration behavior, operational recovery and multi-tenant scale need further acceptance evidence. Financial metrics require suitable cost and baseline data; story points are not financial value.

## Public disclosure boundary

This case study shares reasoning about product management and broad architecture. It excludes proprietary prompts, calculation rules, data models, connector mappings, customer material and internal workflow implementation. Public descriptions cannot guarantee that another team will not develop a similar idea.
