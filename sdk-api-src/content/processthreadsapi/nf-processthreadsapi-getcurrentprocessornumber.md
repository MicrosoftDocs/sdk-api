---
UID: NF:processthreadsapi.GetCurrentProcessorNumber
title: GetCurrentProcessorNumber function
author: windows-sdk-content
description: Retrieves the number of the processor the current thread was running on during the call to this function.
old-location: base\getcurrentprocessornumber.htm
tech.root: procthread
ms.assetid: 1f2bebc7-a548-409a-ab74-78a4b55c8fa7
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetCurrentProcessorNumber, GetCurrentProcessorNumber function, base.getcurrentprocessornumber, processthreadsapi/GetCurrentProcessorNumber, winbase/GetCurrentProcessorNumber
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetCurrentProcessorNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCurrentProcessorNumber function


## -description


Retrieves the number of the processor the current thread was running on during the call to this function.


## -parameters






## -returns



The function returns the current processor number.




## -remarks



This function is used to provide information for estimating process performance.

On systems with more than 64 logical processors, the <b>GetCurrentProcessorNumber</b> function returns the processor number within the <a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">processor group</a> to which the logical processor is assigned. Use the <a href="https://msdn.microsoft.com/46c3d3f7-7a82-40d3-8a9e-0f8d0df534f3">GetCurrentProcessorNumberEx</a> function to retrieve the processor group and number of the current processor.




## -see-also




<a href="https://msdn.microsoft.com/3c9186c8-a54d-4536-8237-bfff78cc7d11">Multiple Processors</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>
 

 

