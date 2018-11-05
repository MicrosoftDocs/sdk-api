---
UID: NS:evntcons._EVENT_EXTENDED_ITEM_STACK_TRACE32
title: "_EVENT_EXTENDED_ITEM_STACK_TRACE32"
author: windows-sdk-content
description: Defines a call stack on a 32-bit computer.
old-location: etw\event_extended_item_stack_trace32.htm
tech.root: etw
ms.assetid: 6898951a-5719-47aa-a219-97f82095686f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PEVENT_EXTENDED_ITEM_STACK_TRACE32, EVENT_EXTENDED_ITEM_STACK_TRACE32, EVENT_EXTENDED_ITEM_STACK_TRACE32 structure [ETW], PEVENT_EXTENDED_ITEM_STACK_TRACE32, PEVENT_EXTENDED_ITEM_STACK_TRACE32 structure pointer [ETW], _EVENT_EXTENDED_ITEM_STACK_TRACE32, etw.event_extended_item_stack_trace32, evntcons/EVENT_EXTENDED_ITEM_STACK_TRACE32, evntcons/PEVENT_EXTENDED_ITEM_STACK_TRACE32"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntcons.h
api_name:
 - EVENT_EXTENDED_ITEM_STACK_TRACE32
product: Windows
targetos: Windows
req.typenames: EVENT_EXTENDED_ITEM_STACK_TRACE32, *PEVENT_EXTENDED_ITEM_STACK_TRACE32
req.redist: 
---

# _EVENT_EXTENDED_ITEM_STACK_TRACE32 structure


## -description


The <b>EVENT_EXTENDED_ITEM_STACK_TRACE32</b> structure defines a call stack on a 32-bit computer.


## -struct-fields




### -field MatchId

A unique identifier that you use to match the kernel-mode calls to the user-mode calls; the kernel-mode calls and user-mode calls are captured in separate events if the environment prevents both from being captured in the same event. If the kernel-mode and user-mode calls were captured in the same event, the value is zero.

Typically, on 32-bit computers, you can always capture both the kernel-mode and user-mode calls in the same event. However, if you use the frame pointer optimization compiler option, the stack may not be captured, captured incorrectly, or truncated.


### -field Address

An array of call addresses on the stack.


## -remarks



The <b>DataSize</b> member of <a href="https://msdn.microsoft.com/130dc14b-7488-48ab-a31d-310c0f4ee13f">EVENT_HEADER_EXTENDED_DATA_ITEM</a> contains the size of this structure. To determine the number of addresses in the array, subtract <code>sizeof(ULONG64)</code> from <b>DataSize</b> and then divide by <code>sizeof(ULONG)</code>.




## -see-also




<a href="https://msdn.microsoft.com/130dc14b-7488-48ab-a31d-310c0f4ee13f">EVENT_HEADER_EXTENDED_DATA_ITEM</a>
 

 

