---
UID: NS:minidumpapiset._MINIDUMP_READ_MEMORY_FAILURE_CALLBACK
title: MINIDUMP_READ_MEMORY_FAILURE_CALLBACK (minidumpapiset.h)
description: Contains information about a failed memory read operation.helpviewer_keywords: ["*PMINIDUMP_READ_MEMORY_FAILURE_CALLBACK","MINIDUMP_READ_MEMORY_FAILURE_CALLBACK","MINIDUMP_READ_MEMORY_FAILURE_CALLBACK structure","PMINIDUMP_READ_MEMORY_FAILURE_CALLBACK","PMINIDUMP_READ_MEMORY_FAILURE_CALLBACK structure pointer","_MINIDUMP_READ_MEMORY_FAILURE_CALLBACK","base.minidump_read_memory_failure_callback","minidumpapiset/MINIDUMP_READ_MEMORY_FAILURE_CALLBACK","minidumpapiset/PMINIDUMP_READ_MEMORY_FAILURE_CALLBACK"]
old-location: base\minidump_read_memory_failure_callback.htm
tech.root: Debug
ms.assetid: 9710684a-4d08-4ab8-bc33-17c5f01c581f
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_READ_MEMORY_FAILURE_CALLBACK, MINIDUMP_READ_MEMORY_FAILURE_CALLBACK, MINIDUMP_READ_MEMORY_FAILURE_CALLBACK structure, PMINIDUMP_READ_MEMORY_FAILURE_CALLBACK, PMINIDUMP_READ_MEMORY_FAILURE_CALLBACK structure pointer, _MINIDUMP_READ_MEMORY_FAILURE_CALLBACK, base.minidump_read_memory_failure_callback, minidumpapiset/MINIDUMP_READ_MEMORY_FAILURE_CALLBACK, minidumpapiset/PMINIDUMP_READ_MEMORY_FAILURE_CALLBACK'
f1_keywords:
- minidumpapiset/MINIDUMP_READ_MEMORY_FAILURE_CALLBACK
dev_langs:
- c++
req.header: minidumpapiset.h
req.include-header: Dbghelp.h
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
- MINIDUMP_READ_MEMORY_FAILURE_CALLBACK
targetos: Windows
req.typenames: MINIDUMP_READ_MEMORY_FAILURE_CALLBACK, *PMINIDUMP_READ_MEMORY_FAILURE_CALLBACK
req.redist: DbgHelp.dll 6.5 or later
ms.custom: 19H1
---

# MINIDUMP_READ_MEMORY_FAILURE_CALLBACK structure


## -description


Contains information about a failed memory read operation. This structure is used by the <a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a>function when the callback type is ReadMemoryFailureCallback.


## -struct-fields




### -field Offset

The offset of the address for the failed memory read operation.


### -field Bytes

The size of the failed memory read operation, in bytes.


### -field FailureStatus

The resulting error code from the failed memory read operation.


## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_input">MINIDUMP_CALLBACK_INPUT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a>
 

 

