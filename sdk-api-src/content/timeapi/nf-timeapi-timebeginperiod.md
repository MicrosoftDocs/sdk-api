---
UID: NF:timeapi.timeBeginPeriod
title: timeBeginPeriod function
author: windows-sdk-content
description: The timeBeginPeriod function requests a minimum resolution for periodic timers.
old-location: multimedia\timebeginperiod.htm
tech.root: Multimedia
ms.assetid: 7168981c-9af8-4665-88a2-7d96a8f2b273
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "_win32_timeBeginPeriod, mmsystem/timeBeginPeriod, multimedia.timebeginperiod, timeBeginPeriod, timeBeginPeriod function [Windows Multimedia], timeapi/timeBeginPeriod"
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
 - timeBeginPeriod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# timeBeginPeriod function


## -description



The <b>timeBeginPeriod</b> function requests a minimum resolution for periodic timers.




## -parameters




### -param uPeriod

Minimum timer resolution, in milliseconds, for the application or device driver. A lower value specifies a higher (more accurate) resolution.


## -returns



Returns <b>TIMERR_NOERROR</b> if successful or <b>TIMERR_NOCANDO</b> if the resolution specified in <i>uPeriod</i> is out of range.




## -remarks



Call this function immediately before using timer services, and call the <a href="https://msdn.microsoft.com/b06531f9-4fd7-4051-80d4-5a175fdd37e7">timeEndPeriod</a> function immediately after you are finished using the timer services.

You must match each call to <b>timeBeginPeriod</b> with a call to <a href="https://msdn.microsoft.com/b06531f9-4fd7-4051-80d4-5a175fdd37e7">timeEndPeriod</a>, specifying the same minimum resolution in both calls. An application can make multiple <b>timeBeginPeriod</b> calls as long as each call is matched with a call to <b>timeEndPeriod</b>.

This function affects a global Windows setting. Windows uses the lowest value (that is, highest resolution) requested by any process. Setting a higher resolution can improve the accuracy of time-out intervals in wait functions. However, it can also reduce overall system performance, because the thread scheduler switches tasks more often. High resolutions can also prevent the CPU power management system from entering power-saving modes. Setting a higher resolution does not improve the accuracy of the high-resolution performance counter.




## -see-also




<a href="https://msdn.microsoft.com/71680295-7fd3-4a8b-a574-78ea05e1d11d">Multimedia Timer Functions</a>



<a href="https://msdn.microsoft.com/25e0b313-64ff-4f30-ae0a-ac364ce3f0cf">Multimedia Timers</a>
 

 

