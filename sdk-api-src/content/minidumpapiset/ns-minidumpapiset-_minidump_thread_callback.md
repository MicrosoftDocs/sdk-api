---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _MINIDUMP_THREAD_CALLBACK structure


## -description


Contains thread information for the 
<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a> function when the callback type is 
<a href="https://msdn.microsoft.com/c970564d-e1f0-4317-bf66-752b98767451">ThreadCallback</a>.


## -struct-fields




### -field ThreadId

The identifier of the thread.


### -field ThreadHandle

A handle to the thread


### -field Pad

 


### -field Context

A 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">CONTEXT</a> structure that contains the processor-specific data.


### -field SizeOfContext

The size of the returned processor-specific data in the <b>Context</b> member, in bytes.


### -field StackBase

The base address of the thread stack.


### -field StackEnd

The ending address of the thread stack.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">CONTEXT</a>



<a href="https://msdn.microsoft.com/0ce3083c-21c9-48a4-9099-1dab31afcafa">MINIDUMP_CALLBACK_INPUT</a>



<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a>
 

 

