---
UID: NS:minidumpapiset._MINIDUMP_THREAD_LIST
title: "_MINIDUMP_THREAD_LIST"
author: windows-sdk-content
description: Contains a list of threads.
old-location: base\minidump_thread_list_str.htm
tech.root: debug
ms.assetid: aa0491d3-e119-41d0-ab53-a108832745d0
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: "*PMINIDUMP_THREAD_LIST, MINIDUMP_THREAD_LIST, MINIDUMP_THREAD_LIST structure, PMINIDUMP_THREAD_LIST, PMINIDUMP_THREAD_LIST structure pointer, _MINIDUMP_THREAD_LIST, _win32_minidump_thread_list_str, base.minidump_thread_list_str, minidumpapiset/MINIDUMP_THREAD_LIST, minidumpapiset/PMINIDUMP_THREAD_LIST"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MINIDUMP_THREAD_LIST
product: Windows
targetos: Windows
req.typenames: MINIDUMP_THREAD_LIST, *PMINIDUMP_THREAD_LIST
req.redist: DbgHelp.dll 5.1 or later
---

# _MINIDUMP_THREAD_LIST structure


## -description


Contains a list of threads.


## -struct-fields




### -field NumberOfThreads

The number of structures in the <b>Threads</b> array.


### -field Threads

An array of 
<a href="https://msdn.microsoft.com/07d4ba98-e74d-4f50-9afa-d09d93da3d6b">MINIDUMP_THREAD</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>



<a href="https://msdn.microsoft.com/07d4ba98-e74d-4f50-9afa-d09d93da3d6b">MINIDUMP_THREAD</a>
 

 

