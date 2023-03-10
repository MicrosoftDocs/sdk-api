---
UID: NF:profileapi.QueryPerformanceCounter
title: QueryPerformanceCounter function
description: Retrieves the current value of the performance counter, which is a high resolution (&lt;1us) time stamp that can be used for time-interval measurements.
helpviewer_keywords: ["QueryPerformanceCounter","QueryPerformanceCounter function [Windows and Messages]","_win32_QueryPerformanceCounter","_win32_queryperformancecounter_cpp","base.queryperformancecounter","profileapi/QueryPerformanceCounter","winmsg.queryperformancecounter","winui._win32_queryperformancecounter"]
old-location: base\queryperformancecounter.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\timers\timerreference\timerfunctions\queryperformancecounter.htm
ms.date: 6/25/2020
ms.keywords: QueryPerformanceCounter, QueryPerformanceCounter function [Windows and Messages], _win32_QueryPerformanceCounter, _win32_queryperformancecounter_cpp, base.queryperformancecounter, profileapi/QueryPerformanceCounter, winmsg.queryperformancecounter, winui._win32_queryperformancecounter
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: snippet-project
f1_keywords:
 - QueryPerformanceCounter
 - profileapi/QueryPerformanceCounter
dev_langs:
 - c++
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
---

# QueryPerformanceCounter function


## -description

Retrieves the current value of the performance counter, which is a high resolution (&lt;1us) time stamp that can be used for time-interval measurements.

## -parameters

### -param lpPerformanceCount [out]

A pointer to a variable that receives the current performance-counter value, in counts.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. On systems that run Windows XP or later, the function will always succeed and will thus never return zero.

## -remarks

For more info about this function and its usage, see <a href="/windows/desktop/SysInfo/acquiring-high-resolution-time-stamps">Acquiring high-resolution time stamps</a>.

## Examples 

```cpp
// Gets the current number of ticks from QueryPerformanceCounter. Throws an
// exception if the call to QueryPerformanceCounter fails.
static inline int64_t GetTicks()
{
    LARGE_INTEGER ticks;
    if (!QueryPerformanceCounter(&ticks))
    {
        winrt::throw_last_error();
    }
    return ticks.QuadPart;
}
```

## -see-also

<a href="/windows/desktop/SysInfo/acquiring-high-resolution-time-stamps">Acquiring high-resolution time stamps</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime">GetSystemTimePreciseAsFileTime</a>



<a href="/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter">KeQueryPerformanceCounter</a>



<a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency">QueryPerformanceFrequency</a>



<b>Reference</b>



<a href="/windows/desktop/SysInfo/time">Time</a>



<a href="/windows/win32/winmsg/timers">Timers</a>