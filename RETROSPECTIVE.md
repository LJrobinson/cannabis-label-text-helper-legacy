# Project Retrospective: # Cannabis Compliance Label Helper — Legacy Retrospective

## Context

Around 2017, during the Nevada medical cannabis era, dispensary inventory and compliance workflows still involved a large amount of manual data entry. One recurring task involved taking COA and compliance-related details and entering them into a large free-text label field inside MJFreeway.

The system allowed the work to be completed, but it did not provide strong guardrails around consistency, formatting, or repeated input patterns. That created an opportunity for avoidable human variation.

## Problem

The core problem was not that employees were unwilling or unable to do the work. The problem was that the workflow depended too heavily on each person manually typing or formatting information the same way every time.

That created several risks:

- inconsistent label text
- slower inventory workflows
- avoidable corrections
- higher cognitive load for repetitive compliance-related work
- unnecessary variation between employees doing the same task

The workflow needed a simple way to make the correct output easier to produce.

## Users

The primary users were inventory team members responsible for preparing or entering cannabis compliance label information.

This was not built for engineers, executives, or external customers. It was built for the people doing the repetitive operational work directly.

## Original Workflow

Before the helper existed, users had to manually interpret the required information, type it into a large MJFreeway label-text field, and rely on memory or copied examples to keep formatting consistent.

Because the input area was essentially free text, the POS/compliance system did not prevent formatting drift. Small differences in spacing, wording, order, or missing details could easily appear from person to person.

## Solution

I built a simple browser-based helper that converted repeated form-style inputs into a standardized copy/paste text block.

The tool gave the inventory team a specific URL they could open, fill out, and use to generate consistent label text. Instead of manually remembering the format each time, the user could rely on the tool to produce the expected structure.

The project was intentionally simple:

- static HTML
- inline CSS
- basic JavaScript
- no backend
- no database
- no authentication
- accessible from a shared URL

The simplicity was the point. The tool did not need to be complex to reduce friction.

## Product Decisions

The most important product decision was to standardize the output rather than ask every user to memorize the standard.

Instead of training alone being the solution, the tool embedded the desired behavior into the workflow.

Key decisions included:

- using a browser page so the team could access it easily
- keeping the interface lightweight
- generating a repeatable text block for copy/paste
- reducing free-form typing
- making the correct format the easiest path

The tool acted as a small guardrail around a fragile manual process.

## User Feedback

The first version included a typing timer or speed/high-score mechanic. At the time, I thought this made the repetitive task more engaging and fun.

After watching a coworker use it, I realized the timer created stress rather than value. Not every user prioritized speed, and not every user was comfortable typing quickly. What felt fun to me created pressure for someone else.

That feedback changed how I thought about the tool.

## Iteration

I removed the timer after seeing the negative user impact.

That was an important early product lesson: a feature can be clever and still be wrong for the user.

The purpose of the tool was not to make people type faster. The purpose was to help them complete compliance-related work more consistently and with less stress.

Removing the timer made the tool more aligned with the actual user need.

## Impact

The helper reduced friction in a repetitive inventory/compliance workflow by making standardized label text easier to generate.

The practical impact was:

- less manual formatting
- fewer opportunities for inconsistent entries
- faster copy/paste workflow
- easier onboarding for repeated label-entry tasks
- reduced reliance on memory
- a clearer standard for the inventory team

The project was small, but it addressed a real operational problem at the point where the work was happening.

## What I Would Do Differently Today

If I rebuilt this today, I would approach it with stronger structure and better long-term maintainability.

Potential improvements would include:

- validation for required fields
- clearer error messages
- examples beside each input
- saved templates for repeated product types
- exportable audit logs
- versioned label formats
- unit tests around output generation
- accessibility improvements
- mobile-friendly design
- separation of HTML, CSS, and JavaScript
- a clearer README and documentation from the beginning

I would also avoid gamifying a compliance workflow unless the user benefit was clearly validated first.

## Why This Project Still Matters

This project matters because it shows an early pattern in how I approach operational problems:

1. I noticed a repeated manual workflow.
2. I identified where human variation was causing friction.
3. I built a simple tool to reduce that variation.
4. I watched real users interact with it.
5. I changed the product based on user feedback.

In hindsight, this was an early product-management style project. It combined domain knowledge, workflow observation, user empathy, and lightweight technical execution.

The tool itself was simple, but the thinking behind it still reflects how I approach software and operations today: reduce friction, add guardrails, and make the correct workflow easier to follow.