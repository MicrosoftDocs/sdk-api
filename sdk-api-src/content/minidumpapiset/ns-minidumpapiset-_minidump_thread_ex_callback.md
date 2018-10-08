---
UID: NS:minidumpapiset._MINIDUMP_THREAD_EX_CALLBACK
title: "_MINIDUMP_THREAD_EX_CALLBACK"
author: windows-sdk-content
description: Contains extended thread information for the MiniDumpCallback function when the callback type is ThreadExCallback.
old-location: base\minidump_thread_ex_callback_str.htm
tech.root: debug
ms.assetid: a81856df-14a3-42bc-89dc-9796c7b252be
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: "*PMINIDUMP_THREAD_EX_CALLBACK, MINIDUMP_THREAD_EX_CALLBACK, MINIDUMP_THREAD_EX_CALLBACK structure, PMINIDUMP_THREAD_EX_CALLBACK, PMINIDUMP_THREAD_EX_CALLBACK structure pointer, _MINIDUMP_THREAD_EX_CALLBACK, _win32_minidump_thread_ex_callback_str, base.minidump_thread_ex_callback_str, minidumpapiset/MINIDUMP_THREAD_EX_CALLBACK, minidumpapiset/PMINIDUMP_THREAD_EX_CALLBACK"
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
 - MINIDUMP_THREAD_EX_CALLBACK
product: Windows
targetos: Windows
req.typenames: MINIDUMP_THREAD_EX_CALLBACK, *PMINIDUMP_THREAD_EX_CALLBACK
req.redist: DbgHelp.dll 5.1 or later
---

# _MINIDUMP_THREAD_EX_CALLBACK structure


## -description


Contains extended thread information for the 
<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a> function when the callback type is 
<a href="https://msdn.microsoft.com/c970564d-e1f0-4317-bf66-752b98767451">ThreadExCallback</a>.


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


### -field BackingStoreBase

<b>Intel Itanium:  </b>The base address of the thread backing store.


### -field BackingStoreEnd

<b>Intel Itanium:  </b>The ending address of the thread backing store.


## -see-also




<a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a>



<a href="https://msdn.microsoft.com/0ce3083c-21c9-48a4-9099-1dab31afcafa">MINIDUMP_CALLBACK_INPUT</a>



<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a>
 

 

