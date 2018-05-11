---
UID: NS:minidumpapiset._MINIDUMP_READ_MEMORY_FAILURE_CALLBACK
title: "_MINIDUMP_READ_MEMORY_FAILURE_CALLBACK"
author: windows-driver-content
description: Contains information about a failed memory read operation.
old-location: base\minidump_read_memory_failure_callback.htm
old-project: Debug
ms.assetid: 9710684a-4d08-4ab8-bc33-17c5f01c581f
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: "*PMINIDUMP_READ_MEMORY_FAILURE_CALLBACK, MINIDUMP_READ_MEMORY_FAILURE_CALLBACK, MINIDUMP_READ_MEMORY_FAILURE_CALLBACK structure, PMINIDUMP_READ_MEMORY_FAILURE_CALLBACK, PMINIDUMP_READ_MEMORY_FAILURE_CALLBACK structure pointer, _MINIDUMP_READ_MEMORY_FAILURE_CALLBACK, base.minidump_read_memory_failure_callback, minidumpapiset/MINIDUMP_READ_MEMORY_FAILURE_CALLBACK, minidumpapiset/PMINIDUMP_READ_MEMORY_FAILURE_CALLBACK"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: MINIDUMP_READ_MEMORY_FAILURE_CALLBACK, *PMINIDUMP_READ_MEMORY_FAILURE_CALLBACK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	minidumpapiset.h
api_name:
-	MINIDUMP_READ_MEMORY_FAILURE_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_READ_MEMORY_FAILURE_CALLBACK structure


## -description


Contains information about a failed memory read operation. This structure is used by the <a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a>
			function when the callback type is ReadMemoryFailureCallback.


## -struct-fields




### -field Offset

The offset of the address for the failed memory read operation.


### -field Bytes

The size of the failed memory read operation, in bytes.


### -field FailureStatus

The resulting error code from the failed memory read operation.


## -see-also




<a href="https://msdn.microsoft.com/0ce3083c-21c9-48a4-9099-1dab31afcafa">MINIDUMP_CALLBACK_INPUT</a>



<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a>
 

 

