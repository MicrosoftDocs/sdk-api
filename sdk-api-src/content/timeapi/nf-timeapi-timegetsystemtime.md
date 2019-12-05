---
UID: NF:timeapi.timeGetSystemTime
title: timeGetSystemTime function (timeapi.h)
description: The timeGetSystemTime function retrieves the system time, in milliseconds.
old-location: multimedia\timegetsystemtime.htm
tech.root: Multimedia
ms.assetid: 57871ada-d2b7-48a9-bed0-3780b836c77a
ms.date: 12/05/2018
ms.keywords: _win32_timeGetSystemTime, mmsystem/timeGetSystemTime, multimedia.timegetsystemtime, timeGetSystemTime, timeGetSystemTime function [Windows Multimedia], timeapi/timeGetSystemTime
ms.topic: function
f1_keywords:
- timeapi/timeGetSystemTime
dev_langs:
- c++
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
- timeGetSystemTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# timeGetSystemTime function


## -description



The <b>timeGetSystemTime</b> function retrieves the system time, in milliseconds. The system time is the time elapsed since Windows was started. This function works very much like the <a href="https://docs.microsoft.com/windows/desktop/api/timeapi/nf-timeapi-timegettime">timeGetTime</a> function. See <b>timeGetTime</b> for details of these functions' operation.




## -parameters




### -param pmmt

Pointer to an <a href="https://docs.microsoft.com/previous-versions/dd757347(v=vs.85)">MMTIME</a> structure.
          


### -param cbmmt

Size, in bytes, of the <a href="https://docs.microsoft.com/previous-versions/dd757347(v=vs.85)">MMTIME</a> structure.
          


## -returns



If successful, returns <b>TIMERR_NOERROR</b>. Otherwise, returns an error code.




## -remarks



The system time is returned in the <b>ms</b> member of the <a href="https://docs.microsoft.com/previous-versions/dd757347(v=vs.85)">MMTIME</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/multimedia-timer-functions">Multimedia Timer Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/multimedia-timers">Multimedia Timers</a>
 

 

