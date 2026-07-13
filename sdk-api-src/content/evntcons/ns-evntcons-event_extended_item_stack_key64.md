---
UID: NS:evntcons._EVENT_EXTENDED_ITEM_STACK_KEY64
tech.root: ETW
title: EVENT_EXTENDED_ITEM_STACK_KEY64 (evntcons.h)
ms.date: 11/28/2022
ms.keywords: _EVENT_EXTENDED_ITEM_STACK_KEY64
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
req.typenames: EVENT_EXTENDED_ITEM_STACK_KEY64, *PEVENT_EXTENDED_ITEM_STACK_KEY64
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - evntcons.h
api_name:
 - _EVENT_EXTENDED_ITEM_STACK_KEY64
 - PEVENT_EXTENDED_ITEM_STACK_KEY64
 - EVENT_EXTENDED_ITEM_STACK_KEY64
f1_keywords:
 - _EVENT_EXTENDED_ITEM_STACK_KEY64
 - evntcons/_EVENT_EXTENDED_ITEM_STACK_KEY64
 - PEVENT_EXTENDED_ITEM_STACK_KEY64
 - evntcons/PEVENT_EXTENDED_ITEM_STACK_KEY64
 - EVENT_EXTENDED_ITEM_STACK_KEY64
 - evntcons/EVENT_EXTENDED_ITEM_STACK_KEY64
dev_langs:
 - c++
helpviewer_keywords:
 - _EVENT_EXTENDED_ITEM_STACK_KEY64
---

# EVENT_EXTENDED_ITEM_STACK_KEY64 structure (evntcons.h)

## -description

Defines an extended item stack key on a 64-bit computer.

## -struct-fields

### -field MatchId

A unique identifier that you use to match the kernel-mode calls to the user-mode calls; the kernel-mode calls and user-mode calls are captured in separate events if the environment prevents both from being captured in the same event. If the kernel-mode and user-mode calls were captured in the same event, the value is zero.

### -field StackKey

The key.

## -remarks

## -see-also
