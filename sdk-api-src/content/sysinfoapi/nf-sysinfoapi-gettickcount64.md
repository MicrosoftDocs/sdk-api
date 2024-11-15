---
UID: NF:sysinfoapi.GetTickCount64
title: GetTickCount64 function (sysinfoapi.h)
description: Retrieves the number of milliseconds that have elapsed since the system was started.
helpviewer_keywords: ["GetTickCount64","GetTickCount64 function","base.gettickcount64","sysinfoapi/GetTickCount64"]
old-location: base\gettickcount64.htm
tech.root: winprog
ms.assetid: 3ebf05b9-cc53-43ae-bbcb-7841793a9d84
ms.date: 12/05/2018
ms.keywords: GetTickCount64, GetTickCount64 function, base.gettickcount64, sysinfoapi/GetTickCount64
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - GetTickCount64
 - sysinfoapi/GetTickCount64
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
 - GetTickCount64
---

# GetTickCount64 function


## -description

Retrieves the number of milliseconds that have elapsed since the system was started.



## -returns

The number of milliseconds.

## -remarks

The resolution of the <b>GetTickCount64</b> function is limited to the resolution of the system timer, which is typically in the range of  10 milliseconds to 16 milliseconds. The resolution of the <b>GetTickCount64</b> function is not affected by adjustments made by the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment">GetSystemTimeAdjustment</a> function.

If you need a higher resolution timer, use a 
<a href="/windows/desktop/Multimedia/multimedia-timers">multimedia timer</a> or a 
<a href="/windows/desktop/winmsg/about-timers">high-resolution timer</a>.

To obtain the time the system has spent in the working state since it was started, use the <a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime">QueryUnbiasedInterruptTime</a> function. 

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime">QueryUnbiasedInterruptTime</a> function produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days. This helps to identify bugs that might not occur until the system has been running for a long time.</div>
<div> </div>
To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>



<a href="/windows/desktop/SysInfo/windows-time">Windows Time</a>
