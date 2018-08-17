---
UID: NS:minidumpapiset._MINIDUMP_THREAD_EX_LIST
title: "_MINIDUMP_THREAD_EX_LIST"
author: windows-sdk-content
description: Contains a list of threads.
old-location: base\minidump_thread_ex_list_str.htm
old-project: debug
ms.assetid: 653f1079-07c9-43b9-8dfe-05e99b365bdc
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PMINIDUMP_THREAD_EX_LIST, MINIDUMP_THREAD_EX_LIST, MINIDUMP_THREAD_EX_LIST structure, PMINIDUMP_THREAD_EX_LIST, PMINIDUMP_THREAD_EX_LIST structure pointer, _MINIDUMP_THREAD_EX_LIST, _win32_minidump_thread_ex_list_str, base.minidump_thread_ex_list_str, minidumpapiset/MINIDUMP_THREAD_EX_LIST, minidumpapiset/PMINIDUMP_THREAD_EX_LIST"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
req.redist: DbgHelp.dll 5.1 or later
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
tech.root: 
req.typenames: MINIDUMP_THREAD_EX_LIST, *PMINIDUMP_THREAD_EX_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_THREAD_EX_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_THREAD_EX_LIST structure


## -description


Contains a list of threads.


## -struct-fields




### -field NumberOfThreads

The number of structures in the <b>Threads</b> array.


### -field Threads

An array of 
<a href="https://msdn.microsoft.com/aa99bdf3-29b7-4865-8935-810388f3d2b3">MINIDUMP_THREAD_EX</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>



<a href="https://msdn.microsoft.com/aa99bdf3-29b7-4865-8935-810388f3d2b3">MINIDUMP_THREAD_EX</a>
 

 

