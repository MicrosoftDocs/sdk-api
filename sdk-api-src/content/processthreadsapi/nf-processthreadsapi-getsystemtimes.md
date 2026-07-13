---
UID: NF:processthreadsapi.GetSystemTimes
title: GetSystemTimes function (processthreadsapi.h)
description: Retrieves system timing information. On a multiprocessor system, the values returned are the sum of the designated times across all processors.
helpviewer_keywords: ["GetSystemTimes","GetSystemTimes function","base.getsystemtimes","processthreadsapi/GetSystemTimes"]
old-location: base\getsystemtimes.htm
tech.root: processthreadsapi
ms.assetid: 84f674e7-536b-4ae0-b523-6a17cb0a1c17
ms.date: 08/08/2025
ms.keywords: GetSystemTimes, GetSystemTimes function, base.getsystemtimes, processthreadsapi/GetSystemTimes
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
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
 - GetSystemTimes
 - processthreadsapi/GetSystemTimes
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
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetSystemTimes
---

# GetSystemTimes function

## -description

Retrieves system timing information in "ticks" (or 100-nanosecond intervals).

## -parameters

### -param lpIdleTime [out, optional]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the amount of time in "ticks" that the system has been idle.

### -param lpKernelTime [out, optional]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the amount of time in "ticks" that the system has spent executing in Kernel mode (including all threads in all processes, on all processors). This time value also includes the amount of time the system has been idle.

### -param lpUserTime [out, optional]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the amount of time in "ticks" that the system has spent executing in User mode (including all threads in all processes, on all processors).

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error  information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

On a multiprocessor system (with 64 processors or fewer), the value returned is the sum of the designated times in "ticks" across all processors.

> [!NOTE]
> On systems with more than 64 processors, the value returned is the sum of the designated times for the primary processor group that the calling thread belongs to (see [Processor Groups](/windows/win32/procthread/processor-groups)).

To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

## -see-also

[FILETIME](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

[System Time](/windows/desktop/SysInfo/system-time)

[Time Functions](/windows/desktop/SysInfo/time-functions)
