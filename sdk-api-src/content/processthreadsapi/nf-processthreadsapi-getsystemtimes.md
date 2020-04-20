---
UID: NF:processthreadsapi.GetSystemTimes
title: GetSystemTimes function (processthreadsapi.h)
description: Retrieves system timing information. On a multiprocessor system, the values returned are the sum of the designated times across all processors.helpviewer_keywords: ["GetSystemTimes","GetSystemTimes function","base.getsystemtimes","processthreadsapi/GetSystemTimes"]
old-location: base\getsystemtimes.htm
tech.root: SysInfo
ms.assetid: 84f674e7-536b-4ae0-b523-6a17cb0a1c17
ms.date: 12/05/2018
ms.keywords: GetSystemTimes, GetSystemTimes function, base.getsystemtimes, processthreadsapi/GetSystemTimes
f1_keywords:
- processthreadsapi/GetSystemTimes
dev_langs:
- c++
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
- GetSystemTimes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetSystemTimes function


## -description


Retrieves system timing information.  On a multiprocessor system, the values returned are the sum
    of the designated times across all processors.


## -parameters




### -param lpIdleTime [out, optional]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the amount of time that the system has been idle.


### -param lpKernelTime [out, optional]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the amount of time that the system has spent executing in Kernel mode (including all threads in all processes, on all processors). This time value also includes the amount of time the system has been idle.


### -param lpUserTime [out, optional]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the amount of time that the system has spent executing in User mode (including all threads in all processes, on all processors).


## -returns



If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error  information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/system-time">System Time</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/time-functions">Time Functions</a>
 

 

