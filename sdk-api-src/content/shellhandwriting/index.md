---
UID: NA:shellhandwriting
title: Shellhandwriting.h header
description: Enables inking with a pen on, or near, any text edit control without first setting focus to the control.
ms.date: 11/13/2023
prerelease: false
ms.keywords: 
ms.topic: overview
ms.update-cycle: 1095-days
tech.root: input_ink
f1_keywords:
 - shellhandwriting
 - shellhandwriting/shellhandwriting
---

# Shellhandwriting.h header

## -description

Enables inking with a pen on, or near, any text edit control without first setting focus to the control. The system determines intent, identifies an input target, renders the ink strokes, recognizes the ink as text (or a gesture for modifying text), suggests text candidates when available, and inserts the new or modified text into the edit field of the control.

This header is used by Ink input. For more information, see:

- [Ink input](../_input_ink/index.md)

Both the Text Services Framework (TSF) and UI Automation (UIA) are used to support ShellHandwriting functionality.

The following steps describe the basic process used for ShellHandwriting functionality.

1. **Opt-out determination:** Determine if application supports ShellHandwriting. Typically applications that do not have robust UI Automation (UIA) implementations or those with custom ink handling.  
2. **Intent determination:** If app supports ShellHandwriting, system determines whether the pen down pointer input should be passed to through to the app or used for handwriting.
3. **Tap determination:** If pen input should be used for handwriting, test whether the input was received by an actionable control (such as a button, which would take input precedence) and whether a control capable of receiving text (Edit, ComboBox, or Document types) can be found that is enabled, not read-only, and able to accept keyboard focus.
4. **Target determination:** If input can be used for handwriting, a bounding box is created around a portion of the input to determine the edit control best suited to receiving the ink recognition results (target determination).
5. **Final determination:** When a target edit control is identified and given focus, various other context indicators (such as input scope, language, existing text bounding rects) are used to confirm appropriateness before the ink recognition results are copied to the control.
