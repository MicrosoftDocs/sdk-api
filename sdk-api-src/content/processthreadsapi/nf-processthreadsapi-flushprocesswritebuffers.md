---
UID: NF:processthreadsapi.FlushProcessWriteBuffers
title: FlushProcessWriteBuffers function (processthreadsapi.h)
description: Flushes the write queue of each processor that is running a thread of the current process.
helpviewer_keywords: ["FlushProcessWriteBuffers","FlushProcessWriteBuffers function","base.flushprocesswritebuffers","processthreadsapi/FlushProcessWriteBuffers","winbase/FlushProcessWriteBuffers"]
old-location: base\flushprocesswritebuffers.htm
tech.root: processthreadsapi
ms.assetid: 6dcf6851-59ee-4f6e-b2cb-e36ac5328b92
ms.date: 12/05/2018
ms.keywords: FlushProcessWriteBuffers, FlushProcessWriteBuffers function, base.flushprocesswritebuffers, processthreadsapi/FlushProcessWriteBuffers, winbase/FlushProcessWriteBuffers
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FlushProcessWriteBuffers
 - processthreadsapi/FlushProcessWriteBuffers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - FlushProcessWriteBuffers
---

# FlushProcessWriteBuffers function


## -description

Flushes the write queue of each processor that is running a thread of the current process.



## -remarks

The function generates an interprocessor interrupt (IPI) to all processors that are part of the current process affinity. It guarantees the visibility of write operations performed on one processor to the other processors.

## -see-also

<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
