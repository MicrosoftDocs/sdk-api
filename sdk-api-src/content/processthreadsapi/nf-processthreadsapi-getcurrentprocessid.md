---
UID: NF:processthreadsapi.GetCurrentProcessId
title: GetCurrentProcessId function
author: windows-sdk-content
description: Retrieves the process identifier of the calling process.
old-location: base\getcurrentprocessid.htm
tech.root: ProcThread
ms.assetid: a442e147-0db0-4911-94de-91728a4b277a
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetCurrentProcessId, GetCurrentProcessId function, _win32_getcurrentprocessid, base.getcurrentprocessid, processthreadsapi/GetCurrentProcessId, winbase/GetCurrentProcessId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetCurrentProcessId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCurrentProcessId function


## -description


Retrieves the process identifier of the calling process.


## -parameters






## -returns



The return value is the process identifier of the calling process.




## -remarks



Until the process terminates, the process identifier uniquely identifies the process throughout the system.




## -see-also




<a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a>



<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>
 

 

