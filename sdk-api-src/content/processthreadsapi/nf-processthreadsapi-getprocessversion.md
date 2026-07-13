---
UID: NF:processthreadsapi.GetProcessVersion
title: GetProcessVersion function (processthreadsapi.h)
description: Retrieves the major and minor version numbers of the system on which the specified process expects to run.
helpviewer_keywords: ["GetProcessVersion","GetProcessVersion function","_win32_getprocessversion","base.getprocessversion","processthreadsapi/GetProcessVersion","winbase/GetProcessVersion"]
old-location: base\getprocessversion.htm
tech.root: processthreadsapi
ms.assetid: ed12f2e5-1674-4885-878f-9ba39415780c
ms.date: 12/05/2018
ms.keywords: GetProcessVersion, GetProcessVersion function, _win32_getprocessversion, base.getprocessversion, processthreadsapi/GetProcessVersion, winbase/GetProcessVersion
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - GetProcessVersion
 - processthreadsapi/GetProcessVersion
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
 - GetProcessVersion
---

# GetProcessVersion function

## -description

Retrieves the major and minor version numbers of the system on which the specified process expects to run.

## -parameters

### -param ProcessId [in]

The process identifier of the process of interest. A value of zero specifies the calling process.

## -returns

If the function succeeds, the return value is the version of the system on which the process expects to run. The high word of the return value contains the major version number. The low word of the return value contains the minor version number.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The function fails if *ProcessId* is an invalid value.

## -remarks

The **GetProcessVersion** function performs less quickly when *ProcessId* is nonzero, specifying a process other than the calling process.

The version number returned by this function is the version number stamped in the image header of the .exe file the process is running. Linker programs set this value.

If this function is called from a 32-bit application running on WOW64, the specified process must be a 32-bit process or the function fails.

## -see-also

<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>

<a href="/windows/desktop/ProcThread/child-processes">Processes</a>
