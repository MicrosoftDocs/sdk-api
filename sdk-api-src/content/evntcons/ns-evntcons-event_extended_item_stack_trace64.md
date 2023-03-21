---
UID: NS:evntcons._EVENT_EXTENDED_ITEM_STACK_TRACE64
title: EVENT_EXTENDED_ITEM_STACK_TRACE64 (evntcons.h)
description: Defines a call stack on a 64-bit computer.
helpviewer_keywords: ["*PEVENT_EXTENDED_ITEM_STACK_TRACE64","EVENT_EXTENDED_ITEM_STACK_TRACE64","EVENT_EXTENDED_ITEM_STACK_TRACE64 structure [ETW]","PEVENT_EXTENDED_ITEM_STACK_TRACE64","PEVENT_EXTENDED_ITEM_STACK_TRACE64 structure pointer [ETW]","etw.event_extended_item_stack_trace64","evntcons/EVENT_EXTENDED_ITEM_STACK_TRACE64","evntcons/PEVENT_EXTENDED_ITEM_STACK_TRACE64"]
old-location: etw\event_extended_item_stack_trace64.htm
tech.root: ETW
ms.assetid: 3c9e0dcb-1eb9-4c9f-a4c8-5a93566be303
ms.date: 12/05/2018
ms.keywords: '*PEVENT_EXTENDED_ITEM_STACK_TRACE64, EVENT_EXTENDED_ITEM_STACK_TRACE64, EVENT_EXTENDED_ITEM_STACK_TRACE64 structure [ETW], PEVENT_EXTENDED_ITEM_STACK_TRACE64, PEVENT_EXTENDED_ITEM_STACK_TRACE64 structure pointer [ETW], etw.event_extended_item_stack_trace64, evntcons/EVENT_EXTENDED_ITEM_STACK_TRACE64, evntcons/PEVENT_EXTENDED_ITEM_STACK_TRACE64'
req.header: evntcons.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: EVENT_EXTENDED_ITEM_STACK_TRACE64, *PEVENT_EXTENDED_ITEM_STACK_TRACE64
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENT_EXTENDED_ITEM_STACK_TRACE64
 - evntcons/_EVENT_EXTENDED_ITEM_STACK_TRACE64
 - PEVENT_EXTENDED_ITEM_STACK_TRACE64
 - evntcons/PEVENT_EXTENDED_ITEM_STACK_TRACE64
 - EVENT_EXTENDED_ITEM_STACK_TRACE64
 - evntcons/EVENT_EXTENDED_ITEM_STACK_TRACE64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntcons.h
api_name:
 - EVENT_EXTENDED_ITEM_STACK_TRACE64
---

# EVENT_EXTENDED_ITEM_STACK_TRACE64 structure (evntcons.h)

## -description

Defines a call stack on a 64-bit computer.

## -struct-fields

### -field MatchId

A unique identifier that you use to match the kernel-mode calls to the user-mode calls; the kernel-mode calls and user-mode calls are captured in separate events if the environment prevents both from being captured in the same event. If the kernel-mode and user-mode calls were captured in the same event, the value is zero.

### -field Address

An array of call addresses on the stack.

## -remarks

The <b>DataSize</b> member of <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header_extended_data_item">EVENT_HEADER_EXTENDED_DATA_ITEM</a> contains the size of this structure. To determine the number of addresses in the array, subtract <code>sizeof(ULONG64)</code> from <b>DataSize</b> and then divide by <code>sizeof(ULONG64)</code>.

## -see-also

<a href="/windows/desktop/api/evntcons/ns-evntcons-event_header_extended_data_item">EVENT_HEADER_EXTENDED_DATA_ITEM</a>