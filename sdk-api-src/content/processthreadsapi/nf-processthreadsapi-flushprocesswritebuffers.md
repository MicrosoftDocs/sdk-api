---
UID: NF:processthreadsapi.FlushProcessWriteBuffers
title: FlushProcessWriteBuffers function
author: windows-sdk-content
description: Flushes the write queue of each processor that is running a thread of the current process.
old-location: base\flushprocesswritebuffers.htm
old-project: procthread
ms.assetid: 6dcf6851-59ee-4f6e-b2cb-e36ac5328b92
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FlushProcessWriteBuffers, FlushProcessWriteBuffers function, base.flushprocesswritebuffers, processthreadsapi/FlushProcessWriteBuffers, winbase/FlushProcessWriteBuffers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.redist: 
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
tech.root: 
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# FlushProcessWriteBuffers function


## -description


Flushes the write queue of each processor that is running a thread of the current process.


## -parameters






## -returns



This function does not return a value.




## -remarks



The function generates an interprocessor interrupt (IPI) to all processors that are part of the current process affinity. It guarantees the visibility of write operations performed on one processor to the other processors.




## -see-also




<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

