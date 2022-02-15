---
UID: NF:timeapi.timeBeginPeriod
title: timeBeginPeriod function (timeapi.h)
description: The timeBeginPeriod function requests a minimum resolution for periodic timers.
helpviewer_keywords: ["_win32_timeBeginPeriod","mmsystem/timeBeginPeriod","multimedia.timebeginperiod","timeBeginPeriod","timeBeginPeriod function [Windows Multimedia]","timeapi/timeBeginPeriod"]
old-location: multimedia\timebeginperiod.htm
tech.root: Multimedia
ms.assetid: 7168981c-9af8-4665-88a2-7d96a8f2b273
ms.date: 12/05/2018
ms.keywords: _win32_timeBeginPeriod, mmsystem/timeBeginPeriod, multimedia.timebeginperiod, timeBeginPeriod, timeBeginPeriod function [Windows Multimedia], timeapi/timeBeginPeriod
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
 - timeBeginPeriod
 - timeapi/timeBeginPeriod
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
 - timeBeginPeriod
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

Call this function immediately before using timer services, and call the <a href="/windows/desktop/api/timeapi/nf-timeapi-timeendperiod">timeEndPeriod</a> function immediately after you are finished using the timer services.

You must match each call to <b>timeBeginPeriod</b> with a call to <a href="/windows/desktop/api/timeapi/nf-timeapi-timeendperiod">timeEndPeriod</a>, specifying the same minimum resolution in both calls. An application can make multiple <b>timeBeginPeriod</b> calls as long as each call is matched with a call to <b>timeEndPeriod</b>.

Prior to Windows 10, version 2004, this function affects a global Windows setting. For all processes Windows uses the lowest value (that is, highest resolution) requested by any process. Starting with Windows 10, version 2004, this function no longer affects global timer resolution. For processes which call this function, Windows uses the lowest value (that is, highest resolution) requested by any process. For processes which have not called this function, Windows does not guarantee a higher resolution than the default system resolution.

Starting with Windows 11, if a window-owning process becomes fully occluded, minimized, or otherwise invisible or inaudible to the end user, Windows does not guarantee a higher resolution than the default system resolution. See <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation">SetProcessInformation</a> for more information on this behavior.

Setting a higher resolution can improve the accuracy of time-out intervals in wait functions. However, it can also reduce overall system performance, because the thread scheduler switches tasks more often. High resolutions can also prevent the CPU power management system from entering power-saving modes. Setting a higher resolution does not improve the accuracy of the high-resolution performance counter.

## -see-also

<a href="/windows/desktop/Multimedia/multimedia-timer-functions">Multimedia Timer Functions</a>



<a href="/windows/desktop/Multimedia/multimedia-timers">Multimedia Timers</a>
