---
UID: NS:minidumpapiset._MINIDUMP_THREAD_CALLBACK
title: "_MINIDUMP_THREAD_CALLBACK"
author: windows-sdk-content
description: Contains thread information for the MiniDumpCallback function when the callback type is ThreadCallback.
old-location: base\minidump_thread_callback_str.htm
tech.root: debug
ms.assetid: 31da83e6-af8c-440c-b715-78c9c6ac4b9f
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: "*PMINIDUMP_THREAD_CALLBACK, MINIDUMP_THREAD_CALLBACK, MINIDUMP_THREAD_CALLBACK structure, PMINIDUMP_THREAD_CALLBACK, PMINIDUMP_THREAD_CALLBACK structure pointer, _MINIDUMP_THREAD_CALLBACK, _win32_minidump_thread_callback_str, base.minidump_thread_callback_str, minidumpapiset/MINIDUMP_THREAD_CALLBACK, minidumpapiset/PMINIDUMP_THREAD_CALLBACK"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_THREAD_CALLBACK
product: Windows
targetos: Windows
req.typenames: MINIDUMP_THREAD_CALLBACK, *PMINIDUMP_THREAD_CALLBACK
req.redist: DbgHelp.dll 5.1 or later
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
<a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure that contains the processor-specific data.


### -field SizeOfContext

The size of the returned processor-specific data in the <b>Context</b> member, in bytes.


### -field StackBase

The base address of the thread stack.


### -field StackEnd

The ending address of the thread stack.


## -see-also




<a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a>



<a href="https://msdn.microsoft.com/0ce3083c-21c9-48a4-9099-1dab31afcafa">MINIDUMP_CALLBACK_INPUT</a>



<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a>
 

 

