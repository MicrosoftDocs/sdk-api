---
UID: NF:timeapi.timeGetTime
title: timeGetTime function
author: windows-sdk-content
description: The timeGetTime function retrieves the system time, in milliseconds. The system time is the time elapsed since Windows was started.
old-location: multimedia\timegettime.htm
tech.root: Multimedia
ms.assetid: f9d3a7a9-1457-4993-92f1-f888780a565e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_win32_timeGetTime, mmsystem/timeGetTime, multimedia.timegettime, timeGetTime, timeGetTime function [Windows Multimedia], timeapi/timeGetTime"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# timeGetTime function


## -description



The <b>timeGetTime</b> function retrieves the system time, in milliseconds. The system time is the time elapsed since Windows was started.




## -parameters






## -returns



Returns the system time, in milliseconds.




## -remarks



The only difference between this function and the <a href="https://msdn.microsoft.com/57871ada-d2b7-48a9-bed0-3780b836c77a">timeGetSystemTime</a> function is that <b>timeGetSystemTime</b> uses the <a href="https://msdn.microsoft.com/94bb7235-2477-4923-add8-f0c8ac8195c2">MMTIME</a> structure to return the system time. The <b>timeGetTime</b> function has less overhead than <b>timeGetSystemTime</b>.

Note that the value returned by the <b>timeGetTime</b> function is a <b>DWORD</b> value. The return value wraps around to 0 every 2^32 milliseconds, which is about 49.71 days. This can cause problems in code that directly uses the <b>timeGetTime</b> return value in computations, particularly where the value is used to control code execution. You should always use the difference between two <b>timeGetTime</b> return values in computations.

The default precision of the <b>timeGetTime</b> function can be five milliseconds or more, depending on the machine. You can use the <a href="https://msdn.microsoft.com/7168981c-9af8-4665-88a2-7d96a8f2b273">timeBeginPeriod</a> and <a href="https://msdn.microsoft.com/b06531f9-4fd7-4051-80d4-5a175fdd37e7">timeEndPeriod</a> functions to increase the precision of <b>timeGetTime</b>. If you do so, the minimum difference between successive values returned by <b>timeGetTime</b> can be as large as the minimum period value set using <b>timeBeginPeriod</b> and <b>timeEndPeriod</b>. Use the <a href="winmsg.queryperformancecounter">QueryPerformanceCounter</a> and <a href="winmsg.queryperformancefrequency">QueryPerformanceFrequency</a> functions to measure short time intervals at a high resolution.




## -see-also




<a href="https://msdn.microsoft.com/71680295-7fd3-4a8b-a574-78ea05e1d11d">Multimedia Timer Functions</a>



<a href="https://msdn.microsoft.com/25e0b313-64ff-4f30-ae0a-ac364ce3f0cf">Multimedia Timers</a>
 

 

