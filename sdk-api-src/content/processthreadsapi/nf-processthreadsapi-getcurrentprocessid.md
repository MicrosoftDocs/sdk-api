---
UID: NF:processthreadsapi.GetCurrentProcessId
title: GetCurrentProcessId function (processthreadsapi.h)
description: Retrieves the process identifier of the calling process.
helpviewer_keywords: ["GetCurrentProcessId","GetCurrentProcessId function","_win32_getcurrentprocessid","base.getcurrentprocessid","processthreadsapi/GetCurrentProcessId","winbase/GetCurrentProcessId"]
old-location: base\getcurrentprocessid.htm
tech.root: processthreadsapi
ms.assetid: a442e147-0db0-4911-94de-91728a4b277a
ms.date: 12/05/2018
ms.keywords: GetCurrentProcessId, GetCurrentProcessId function, _win32_getcurrentprocessid, base.getcurrentprocessid, processthreadsapi/GetCurrentProcessId, winbase/GetCurrentProcessId
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetCurrentProcessId
 - processthreadsapi/GetCurrentProcessId
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
 - GetCurrentProcessId
---

# GetCurrentProcessId function


## -description

Retrieves the process identifier of the calling process.



## -returns

The return value is the process identifier of the calling process.

## -remarks

Until the process terminates, the process identifier uniquely identifies the process throughout the system.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess">OpenProcess</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>
