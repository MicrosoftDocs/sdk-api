---
UID: NF:sysinfoapi.GetTickCount
title: GetTickCount function (sysinfoapi.h)
description: Retrieves the number of milliseconds that have elapsed since the system was started, up to 49.7 days.
helpviewer_keywords: ["GetTickCount","GetTickCount function","_win32_gettickcount","base.gettickcount","sysinfoapi/GetTickCount"]
old-location: base\gettickcount.htm
tech.root: winprog
ms.assetid: 22201c82-a49a-4972-9f49-6baf6d23a1ea
ms.date: 12/05/2018
ms.keywords: GetTickCount, GetTickCount function, _win32_gettickcount, base.gettickcount, sysinfoapi/GetTickCount
req.header: sysinfoapi.h
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
 - GetTickCount
 - sysinfoapi/GetTickCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetTickCount
---

# GetTickCount function


## -description

Retrieves the number of milliseconds that have elapsed since the system was started, up to 49.7 days.



## -returns

The return value is the number of milliseconds that have elapsed since the system was started.

## -remarks

The resolution of the <b>GetTickCount</b> function is limited to the resolution of the system timer, which is typically in the range of  10 milliseconds to 16 milliseconds. The resolution of the <b>GetTickCount</b> function is not affected by adjustments made by the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment">GetSystemTimeAdjustment</a> function.

The elapsed time is stored as a <b>DWORD</b> value. Therefore, the time will wrap around to zero if the system is run continuously for 49.7 days. To avoid this problem, use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount64">GetTickCount64</a> function. Otherwise, check for an overflow condition when comparing times.

If you need a higher resolution timer, use a 
<a href="/windows/desktop/Multimedia/multimedia-timers">multimedia timer</a> or a 
<a href="/windows/desktop/winmsg/about-timers">high-resolution timer</a>.

To obtain the time elapsed since the computer was started, retrieve the System Up Time counter in the performance data in the registry key <b>HKEY_PERFORMANCE_DATA</b>. The value returned is an 8-byte value. For more information, see 
<a href="/windows/desktop/PerfCtrs/performance-counters-portal">Performance Counters</a>. 

To obtain the time the system has spent in the working state since it was started, use the <a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime">QueryUnbiasedInterruptTime</a> function.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime">QueryUnbiasedInterruptTime</a> function produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days. This helps to identify bugs that might not occur until the system has been running for a long time.</div>
<div> </div>

## Examples

```cpp
// calculate a 't' value that will linearly interpolate from 0 to 1 and back every 20 seconds
DWORD currentTime = GetTickCount();
if ( m_startTime == 0 )
{
    m_startTime = currentTime;
}
float t = 2 * (( currentTime - m_startTime) % 20000) / 20000.0f;
if (t > 1.0f)
{
    t = 2 - t;
}
```


## -see-also

<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>



<a href="/windows/desktop/SysInfo/windows-time">Windows Time</a>
