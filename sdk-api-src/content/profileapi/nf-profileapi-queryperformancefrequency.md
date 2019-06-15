---
UID: NF:profileapi.QueryPerformanceFrequency
title: QueryPerformanceFrequency function
author: windows-sdk-content
description: Retrieves the frequency of the performance counter.
old-location: base\queryperformancefrequency.htm
tech.root: SysInfo
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\timers\timerreference\timerfunctions\queryperformancefrequency.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: QueryPerformanceFrequency, QueryPerformanceFrequency function [Windows and Messages], _win32_QueryPerformanceFrequency, _win32_queryperformancefrequency_cpp, base.queryperformancefrequency, profileapi/QueryPerformanceFrequency, winmsg.queryperformancefrequency, winui._win32_queryperformancefrequency
ms.topic: function
req.header: profileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-profile-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - QueryPerformanceFrequency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# QueryPerformanceFrequency function


## -description


Retrieves the frequency of the performance counter. The frequency of the performance counter is fixed at system boot and is consistent across all processors. Therefore, the frequency need only be queried upon application initialization, and the result can be cached.


## -parameters




### -param lpFrequency [out]

A pointer to a variable that receives the current performance-counter frequency, in counts per second. If the installed hardware doesn't support a high-resolution performance counter, this parameter can be zero (this will not occur on systems that run Windows XP or later).


## -returns



If the installed hardware supports a high-resolution performance counter, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. On systems that run Windows XP or later, the function will always succeed and will thus never return zero.




## -remarks



For more info about this function and its usage, see <a href="https://docs.microsoft.com/windows/desktop/SysInfo/acquiring-high-resolution-time-stamps">Acquiring high-resolution time stamps</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SysInfo/acquiring-high-resolution-time-stamps">Acquiring high-resolution time stamps</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime">GetSystemTimePreciseAsFileTime</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter">KeQueryPerformanceCounter</a>



<a href="https://msdn.microsoft.com/08169390-940b-4110-813a-249d107cc953">QueryPerformanceCounter</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/time">Time</a>



<a href="https://msdn.microsoft.com/be335927-a78d-4023-bedb-94aaf3a561ae">Timers</a>
 

 

