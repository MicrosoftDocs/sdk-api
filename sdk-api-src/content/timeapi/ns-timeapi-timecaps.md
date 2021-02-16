---
UID: NS:timeapi.timecaps_tag
title: TIMECAPS (timeapi.h)
description: The TIMECAPS structure contains information about the resolution of the timer.
helpviewer_keywords: ["*LPTIMECAPS","*NPTIMECAPS","*PTIMECAPS","LPTIMECAPS","LPTIMECAPS structure pointer [Windows Multimedia]","NPTIMECAPS","NPTIMECAPS structure pointer [Windows Multimedia]","PTIMECAPS","PTIMECAPS structure pointer [Windows Multimedia]","TIMECAPS","TIMECAPS structure [Windows Multimedia]","_win32_TIMECAPS_str","mmsystem/LPTIMECAPS","mmsystem/NPTIMECAPS","mmsystem/PTIMECAPS","mmsystem/TIMECAPS","multimedia.timecaps","timeapi/LPTIMECAPS","timeapi/NPTIMECAPS","timeapi/PTIMECAPS","timeapi/TIMECAPS"]
old-location: multimedia\timecaps.htm
tech.root: Multimedia
ms.assetid: 64a5c4ba-d340-4abc-8da3-766f3a2d7ec8
ms.date: 12/05/2018
ms.keywords: '*LPTIMECAPS, *NPTIMECAPS, *PTIMECAPS, LPTIMECAPS, LPTIMECAPS structure pointer [Windows Multimedia], NPTIMECAPS, NPTIMECAPS structure pointer [Windows Multimedia], PTIMECAPS, PTIMECAPS structure pointer [Windows Multimedia], TIMECAPS, TIMECAPS structure [Windows Multimedia], _win32_TIMECAPS_str, mmsystem/LPTIMECAPS, mmsystem/NPTIMECAPS, mmsystem/PTIMECAPS, mmsystem/TIMECAPS, multimedia.timecaps, timeapi/LPTIMECAPS, timeapi/NPTIMECAPS, timeapi/PTIMECAPS, timeapi/TIMECAPS'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TIMECAPS, *PTIMECAPS, *NPTIMECAPS, *LPTIMECAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - timecaps_tag
 - timeapi/timecaps_tag
 - PTIMECAPS
 - timeapi/PTIMECAPS
 - TIMECAPS
 - timeapi/TIMECAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - TimeAPI.h
 - Mmsystem.h
api_name:
 - TIMECAPS
---

# TIMECAPS structure


## -description

The <b>TIMECAPS</b> structure contains information about the resolution of the timer.

## -struct-fields

### -field wPeriodMin

The minimum supported resolution, in milliseconds.

### -field wPeriodMax

The maximum supported resolution, in milliseconds.

## -see-also

<a href="/windows/desktop/Multimedia/multimedia-timer-structures">Multimedia Timer Structures</a>



<a href="/windows/desktop/Multimedia/multimedia-timers">Multimedia Timers</a>



<a href="/windows/desktop/Multimedia/timer-resolution">Timer Resolution</a>



<a href="/windows/desktop/api/timeapi/nf-timeapi-timegetdevcaps">timeGetDevCaps</a>