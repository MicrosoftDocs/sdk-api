---
UID: NF:processthreadsapi.GetThreadInformation
title: GetThreadInformation function
author: windows-sdk-content
description: Retrieves information about the specified thread.
old-location: base\getthreadinformation.htm
tech.root: procthread
ms.assetid: b7996647-78ab-4f32-bcf6-41aa87d13bb8
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: GetThreadInformation, GetThreadInformation function, base.getthreadinformation, processthreadsapi/GetThreadInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetThreadInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetThreadInformation function


## -description


Retrieves information about the specified thread.


## -parameters




### -param hThread [in]

A handle to the thread. The handle must have THREAD_QUERY_INFORMATION access rights. For more information, see  <a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.


### -param ThreadInformationClass [in]

The class of information to retrieve. The only supported values are <b>ThreadMemoryPriority</b> and <b>ThreadPowerThrottling</b>.


### -param ThreadInformation

Pointer to a structure to receive the type of information specified by the <i>ThreadInformationClass</i> parameter.

If the <i>ThreadInformationClass</i> parameter is <b>ThreadMemoryPriority</b>, this parameter must point to a <b>MEMORY_PRIORITY_INFORMATION</b> structure.

If the <i>ThreadInformationClass</i> parameter is <b>ThreadPowerThrottling</b>, this parameter must point to a <b>THREAD_POWER_THROTTLING_STATE</b> structure.


### -param ThreadInformationSize [in]

The size in bytes of the structure specified by the <i>ThreadInformation</i> parameter.

If the <i>ThreadInformationClass</i> parameter is <b>ThreadMemoryPriority</b>, this parameter must be <code>sizeof(MEMORY_PRIORITY_INFORMATION)</code>.  

If the <i>ThreadInformationClass</i> parameter is <b>ThreadPowerThrottling</b>, this parameter must be <code>sizeof(THREAD_POWER_THROTTLING_STATE)</code>.  


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/2b075405-b7b6-4da0-b78d-45eaa9c6c8cd">GetProcessInformation</a>



<a href="https://msdn.microsoft.com/c0159bea-870a-46b7-a350-91fe52efae49">SetThreadInformation</a>
 

 

