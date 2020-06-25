---
UID: NF:processthreadsapi.GetThreadInformation
title: GetThreadInformation function (processthreadsapi.h)
description: Retrieves information about the specified thread.
helpviewer_keywords: ["GetThreadInformation","GetThreadInformation function","base.getthreadinformation","processthreadsapi/GetThreadInformation"]
old-location: base\getthreadinformation.htm
tech.root: ProcThread
ms.assetid: b7996647-78ab-4f32-bcf6-41aa87d13bb8
ms.date: 12/05/2018
ms.keywords: GetThreadInformation, GetThreadInformation function, base.getthreadinformation, processthreadsapi/GetThreadInformation
f1_keywords:
- processthreadsapi/GetThreadInformation
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetThreadInformation function


## -description


Retrieves information about the specified thread.


## -parameters




### -param hThread [in]

A handle to the thread. The handle must have THREAD_QUERY_INFORMATION access rights. For more information, see  <a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.


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
      <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessinformation">GetProcessInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadinformation">SetThreadInformation</a>
 

 

