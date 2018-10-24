---
UID: NF:processthreadsapi.GetCurrentProcessorNumberEx
title: GetCurrentProcessorNumberEx function
author: windows-sdk-content
description: Retrieves the processor group and number of the logical processor in which the calling thread is running.
old-location: base\getcurrentprocessornumberex.htm
tech.root: ProcThread
ms.assetid: 46c3d3f7-7a82-40d3-8a9e-0f8d0df534f3
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetCurrentProcessorNumberEx, GetCurrentProcessorNumberEx function, base.getcurrentprocessornumberex, processthreadsapi/GetCurrentProcessorNumberEx, winbase/GetCurrentProcessorNumberEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetCurrentProcessorNumberEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCurrentProcessorNumberEx function


## -description


Retrieves the processor group and number of the logical processor in which the calling thread is running.


## -parameters




### -param ProcNumber [out]

A pointer to a <a href="https://msdn.microsoft.com/9005c6d4-07a9-4ce0-9ee2-54880d7244c3">PROCESSOR_NUMBER</a> structure that receives the processor group to which the logical processor is assigned and the number of the logical processor within its group. 


## -returns



If the function succeeds, the <i>ProcNumber</i> parameter contains the group and processor number of the processor on which the calling thread is running. 




## -remarks



To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.



