---
UID: NF:profileapi.QueryPerformanceCounter
title: QueryPerformanceCounter function
description: Retrieves the current value of the performance counter, which is a high resolution (&lt;1us) time stamp that can be used for time-interval measurements.
old-location: base\queryperformancecounter.htm
tech.root: SysInfo
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\timers\timerreference\timerfunctions\queryperformancecounter.htm
ms.date: 12/05/2018
ms.keywords: QueryPerformanceCounter, QueryPerformanceCounter function [Windows and Messages], _win32_QueryPerformanceCounter, _win32_queryperformancecounter_cpp, base.queryperformancecounter, profileapi/QueryPerformanceCounter, winmsg.queryperformancecounter, winui._win32_queryperformancecounter
f1_keywords:
- profileapi/QueryPerformanceCounter
dev_langs:
- c++
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
- QueryPerformanceCounter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# QueryPerformanceCounter function


## -description


Retrieves the current value of the performance counter, which is a high resolution (&lt;1us) time stamp that can be used for time-interval measurements.


## -parameters




### -param lpPerformanceCount [out]

A pointer to a variable that receives the current performance-counter value, in counts. 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. On systems that run Windows XP or later, the function will always succeed and will thus never return zero.




## -remarks



For more info about this function and its usage, see <a href="https://docs.microsoft.com/windows/desktop/SysInfo/acquiring-high-resolution-time-stamps">Acquiring high-resolution time stamps</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SysInfo/acquiring-high-resolution-time-stamps">Acquiring high-resolution time stamps</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime">GetSystemTimePreciseAsFileTime</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter">KeQueryPerformanceCounter</a>



<a href="https://msdn.microsoft.com/f69367a4-0516-4033-81e3-90d4c5270a1e">QueryPerformanceFrequency</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/time">Time</a>



<a href="https://msdn.microsoft.com/be335927-a78d-4023-bedb-94aaf3a561ae">Timers</a>
 

 

