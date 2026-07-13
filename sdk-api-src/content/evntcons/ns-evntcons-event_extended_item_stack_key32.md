---
UID: NS:evntcons._EVENT_EXTENDED_ITEM_STACK_KEY32
tech.root: ETW
title: EVENT_EXTENDED_ITEM_STACK_KEY32 (evntcons.h)
ms.date: 11/28/2022
ms.keywords: _EVENT_EXTENDED_ITEM_STACK_KEY32
targetos: Windows
description: 
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: evntcons.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.target-type: Windows
req.typenames: EVENT_EXTENDED_ITEM_STACK_KEY32, *PEVENT_EXTENDED_ITEM_STACK_KEY32
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - evntcons.h
api_name:
 - _EVENT_EXTENDED_ITEM_STACK_KEY32
 - PEVENT_EXTENDED_ITEM_STACK_KEY32
 - EVENT_EXTENDED_ITEM_STACK_KEY32
f1_keywords:
 - _EVENT_EXTENDED_ITEM_STACK_KEY32
 - evntcons/_EVENT_EXTENDED_ITEM_STACK_KEY32
 - PEVENT_EXTENDED_ITEM_STACK_KEY32
 - evntcons/PEVENT_EXTENDED_ITEM_STACK_KEY32
 - EVENT_EXTENDED_ITEM_STACK_KEY32
 - evntcons/EVENT_EXTENDED_ITEM_STACK_KEY32
dev_langs:
 - c++
helpviewer_keywords:
 - _EVENT_EXTENDED_ITEM_STACK_KEY32
---

# EVENT_EXTENDED_ITEM_STACK_KEY32 structure (evntcons.h)

## -description

Defines an extended item stack key on a 32-bit computer.

## -struct-fields

### -field MatchId

A unique identifier that you use to match the kernel-mode calls to the user-mode calls; the kernel-mode calls and user-mode calls are captured in separate events if the environment prevents both from being captured in the same event. If the kernel-mode and user-mode calls were captured in the same event, the value is zero.

Typically, on 32-bit computers, you can always capture both the kernel-mode and user-mode calls in the same event. However, if you use the frame pointer optimization compiler option, the stack may not be captured, captured incorrectly, or truncated.

### -field StackKey

The key.

### -field Padding

The key padding.

## -remarks

## -see-also
