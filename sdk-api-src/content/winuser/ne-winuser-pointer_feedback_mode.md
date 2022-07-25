---
UID: NE:winuser.__unnamed_enum_0
title: POINTER_FEEDBACK_MODE (winuser.h)
description: Identifies the visual feedback behaviors available to CreateSyntheticPointerDevice.
helpviewer_keywords: ["POINTER_FEEDBACK_DEFAULT","POINTER_FEEDBACK_INDIRECT","POINTER_FEEDBACK_MODE","POINTER_FEEDBACK_MODE enumeration","POINTER_FEEDBACK_NONE","input_pointerdevice.pointer_feedback_mode","winuser/POINTER_FEEDBACK_DEFAULT","winuser/POINTER_FEEDBACK_INDIRECT","winuser/POINTER_FEEDBACK_MODE","winuser/POINTER_FEEDBACK_NONE"]
old-location: input_pointerdevice\pointer_feedback_mode.htm
tech.root: controls
ms.assetid: 73D024E9-F83B-408F-BC96-6851AB4603AE
ms.date: 12/05/2018
ms.keywords: POINTER_FEEDBACK_DEFAULT, POINTER_FEEDBACK_INDIRECT, POINTER_FEEDBACK_MODE, POINTER_FEEDBACK_MODE enumeration, POINTER_FEEDBACK_NONE, input_pointerdevice.pointer_feedback_mode, winuser/POINTER_FEEDBACK_DEFAULT, winuser/POINTER_FEEDBACK_INDIRECT, winuser/POINTER_FEEDBACK_MODE, winuser/POINTER_FEEDBACK_NONE
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: POINTER_FEEDBACK_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - POINTER_FEEDBACK_MODE
 - winuser/POINTER_FEEDBACK_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - POINTER_FEEDBACK_MODE
---

# POINTER_FEEDBACK_MODE enumeration


## -description

Identifies the visual feedback behaviors available to <a href="../winuser/nf-winuser-createsyntheticpointerdevice.md">CreateSyntheticPointerDevice</a>.

## -enum-fields

### -field POINTER_FEEDBACK_DEFAULT:1

Visual feedback might be suppressed by the user's pen (Settings -&gt; Devices -&gt; Pen &amp; Windows Ink) and touch (Settings -&gt; Ease of Access -&gt; Cursor &amp; pointer size) settings.

### -field POINTER_FEEDBACK_INDIRECT:2

Visual feedback overrides the user's pen and touch settings.

### -field POINTER_FEEDBACK_NONE:3

Visual feedback is disabled.

