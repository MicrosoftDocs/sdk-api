---
UID: NS:evntcons._EVENT_EXTENDED_ITEM_STACK_TRACE64
title: "_EVENT_EXTENDED_ITEM_STACK_TRACE64"
author: windows-sdk-content
description: Defines a call stack on a 64-bit computer.
old-location: etw\event_extended_item_stack_trace64.htm
old-project: ETW
ms.assetid: 3c9e0dcb-1eb9-4c9f-a4c8-5a93566be303
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: "*PEVENT_EXTENDED_ITEM_STACK_TRACE64, EVENT_EXTENDED_ITEM_STACK_TRACE64, EVENT_EXTENDED_ITEM_STACK_TRACE64 structure [ETW], PEVENT_EXTENDED_ITEM_STACK_TRACE64, PEVENT_EXTENDED_ITEM_STACK_TRACE64 structure pointer [ETW], _EVENT_EXTENDED_ITEM_STACK_TRACE64, etw.event_extended_item_stack_trace64, evntcons/EVENT_EXTENDED_ITEM_STACK_TRACE64, evntcons/PEVENT_EXTENDED_ITEM_STACK_TRACE64"
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
tech.root: 
req.typenames: EVENT_EXTENDED_ITEM_STACK_TRACE64, *PEVENT_EXTENDED_ITEM_STACK_TRACE64
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntcons.h
api_name:
 - EVENT_EXTENDED_ITEM_STACK_TRACE64
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EVENT_EXTENDED_ITEM_STACK_TRACE64 structure


## -description


The  <b>EVENT_EXTENDED_ITEM_STACK_TRACE64</b> structure defines a call stack on a 64-bit computer.


## -struct-fields




### -field MatchId

A unique identifier that you use to match the kernel-mode calls to the user-mode calls; the kernel-mode calls and user-mode calls are captured in separate events if the environment prevents both from being captured in the same event. If the kernel-mode and user-mode calls were captured in the same event, the value is zero.


### -field Address

An array of call addresses on the stack.


## -remarks



The <b>DataSize</b> member of <a href="https://msdn.microsoft.com/130dc14b-7488-48ab-a31d-310c0f4ee13f">EVENT_HEADER_EXTENDED_DATA_ITEM</a> contains the size of this structure. To determine the number of addresses in the array, subtract <code>sizeof(ULONG64)</code> from <b>DataSize</b> and then divide by <code>sizeof(ULONG64)</code>.




## -see-also




<a href="https://msdn.microsoft.com/130dc14b-7488-48ab-a31d-310c0f4ee13f">EVENT_HEADER_EXTENDED_DATA_ITEM</a>
 

 

