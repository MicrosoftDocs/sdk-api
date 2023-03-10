---
UID: NF:timeapi.timeGetTime
title: timeGetTime function (timeapi.h)
description: The timeGetTime function retrieves the system time, in milliseconds. The system time is the time elapsed since Windows was started.
helpviewer_keywords: ["_win32_timeGetTime","mmsystem/timeGetTime","multimedia.timegettime","timeGetTime","timeGetTime function [Windows Multimedia]","timeapi/timeGetTime"]
old-location: multimedia\timegettime.htm
tech.root: Multimedia
ms.assetid: f9d3a7a9-1457-4993-92f1-f888780a565e
ms.date: 12/05/2018
ms.keywords: _win32_timeGetTime, mmsystem/timeGetTime, multimedia.timegettime, timeGetTime, timeGetTime function [Windows Multimedia], timeapi/timeGetTime
req.header: timeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - timeGetTime
 - timeapi/timeGetTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-Time-l1-1-0.dll
 - Kernel32.dll
 - Kernel32legacy.dll
api_name:
 - timeGetTime
---

# timeGetTime function


## -description

The <b>timeGetTime</b> function retrieves the system time, in milliseconds. The system time is the time elapsed since Windows was started.



## -returns

Returns the system time, in milliseconds.

## -remarks

The only difference between this function and the <a href="/windows/desktop/api/timeapi/nf-timeapi-timegetsystemtime">timeGetSystemTime</a> function is that <b>timeGetSystemTime</b> uses the <a href="/previous-versions/dd757347(v=vs.85)">MMTIME</a> structure to return the system time. The <b>timeGetTime</b> function has less overhead than <b>timeGetSystemTime</b>.

Note that the value returned by the <b>timeGetTime</b> function is a <b>DWORD</b> value. The return value wraps around to 0 every 2^32 milliseconds, which is about 49.71 days. This can cause problems in code that directly uses the <b>timeGetTime</b> return value in computations, particularly where the value is used to control code execution. You should always use the difference between two <b>timeGetTime</b> return values in computations.

The default precision of the <b>timeGetTime</b> function can be five milliseconds or more, depending on the machine. You can use the <a href="/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod">timeBeginPeriod</a> and <a href="/windows/desktop/api/timeapi/nf-timeapi-timeendperiod">timeEndPeriod</a> functions to increase the precision of <b>timeGetTime</b>. If you do so, the minimum difference between successive values returned by <b>timeGetTime</b> can be as large as the minimum period value set using <b>timeBeginPeriod</b> and <b>timeEndPeriod</b>. Use the <a href="/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter">QueryPerformanceCounter</a> and <a href="/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency">QueryPerformanceFrequency</a> functions to measure short time intervals at a high resolution.

## -see-also

<a href="/windows/desktop/Multimedia/multimedia-timer-functions">Multimedia Timer Functions</a>



<a href="/windows/desktop/Multimedia/multimedia-timers">Multimedia Timers</a>
