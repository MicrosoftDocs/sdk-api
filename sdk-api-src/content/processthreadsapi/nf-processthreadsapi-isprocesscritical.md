---
UID: NF:processthreadsapi.IsProcessCritical
title: IsProcessCritical function
author: windows-sdk-content
description: Determines whether the specified process is considered critical.
old-location: base\isprocesscritical.htm
tech.root: ProcThread
ms.assetid: A5ED8672-B4C3-4A31-8B3F-A181628219A4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IsProcessCritical, IsProcessCritical function, base.isprocesscritical, processthreadsapi/IsProcessCritical
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.dll: Ntdll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
 - API-MS-Win-Core-Processthreads-l1-1-2.dll
 - Kernel32.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - IsProcessCritical
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- IsProcessCritical
: 
---

# IsProcessCritical function


## -description


Determines whether the specified process is considered critical.


## -parameters




### -param hProcess [in]

A handle to the process to query. The process must have been          opened with <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access.  


### -param Critical [out]

A pointer to the <b>BOOL</b> value this function will use to indicate whether the process          is considered critical.  


## -returns



This routine returns FALSE on failure. Any other value indicates success.      Call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to query for the specific error reason on failure.




## -see-also




<a href="https://msdn.microsoft.com/40e6f80d-a778-4d5f-bb1b-db294815f8b5">HRESULT_FROM_WIN32</a>
 

 

