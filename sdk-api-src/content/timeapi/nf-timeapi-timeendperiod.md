---
UID: NF:timeapi.timeEndPeriod
title: timeEndPeriod function (timeapi.h)
description: The timeEndPeriod function clears a previously set minimum timer resolution.
helpviewer_keywords: ["_win32_timeEndPeriod","mmsystem/timeEndPeriod","multimedia.timeendperiod","timeEndPeriod","timeEndPeriod function [Windows Multimedia]","timeapi/timeEndPeriod"]
old-location: multimedia\timeendperiod.htm
tech.root: Multimedia
ms.assetid: b06531f9-4fd7-4051-80d4-5a175fdd37e7
ms.date: 12/05/2018
ms.keywords: _win32_timeEndPeriod, mmsystem/timeEndPeriod, multimedia.timeendperiod, timeEndPeriod, timeEndPeriod function [Windows Multimedia], timeapi/timeEndPeriod
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
 - timeEndPeriod
 - timeapi/timeEndPeriod
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
 - timeEndPeriod
---

# timeEndPeriod function


## -description

The <b>timeEndPeriod</b> function clears a previously set minimum timer resolution.

## -parameters

### -param uPeriod

Minimum timer resolution specified in the previous call to the <a href="/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod">timeBeginPeriod</a> function.

## -returns

Returns <b>TIMERR_NOERROR</b> if successful or <b>TIMERR_NOCANDO</b> if the resolution specified in uPeriod is out of range.

## -remarks

Call this function immediately after you are finished using timer services.

You must match each call to <a href="/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod">timeBeginPeriod</a> with a call to <b>timeEndPeriod</b>, specifying the same minimum resolution in both calls. An application can make multiple <b>timeBeginPeriod</b> calls as long as each call is matched with a call to <b>timeEndPeriod</b>.

## -see-also

<a href="/windows/desktop/Multimedia/multimedia-timer-functions">Multimedia Timer Functions</a>



<a href="/windows/desktop/Multimedia/multimedia-timers">Multimedia Timers</a>