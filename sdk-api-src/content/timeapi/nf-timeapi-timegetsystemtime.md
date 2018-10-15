---
UID: NF:timeapi.timeGetSystemTime
title: timeGetSystemTime function
author: windows-sdk-content
description: The timeGetSystemTime function retrieves the system time, in milliseconds.
old-location: multimedia\timegetsystemtime.htm
tech.root: Multimedia
ms.assetid: 57871ada-d2b7-48a9-bed0-3780b836c77a
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "_win32_timeGetSystemTime, mmsystem/timeGetSystemTime, multimedia.timegetsystemtime, timeGetSystemTime, timeGetSystemTime function [Windows Multimedia], timeapi/timeGetSystemTime"
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
 - timeGetSystemTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# timeGetSystemTime function


## -description



The <b>timeGetSystemTime</b> function retrieves the system time, in milliseconds. The system time is the time elapsed since Windows was started. This function works very much like the <a href="https://msdn.microsoft.com/f9d3a7a9-1457-4993-92f1-f888780a565e">timeGetTime</a> function. See <b>timeGetTime</b> for details of these functions' operation.




## -parameters




### -param pmmt

Pointer to an <a href="https://msdn.microsoft.com/94bb7235-2477-4923-add8-f0c8ac8195c2">MMTIME</a> structure.
          


### -param cbmmt

Size, in bytes, of the <a href="https://msdn.microsoft.com/94bb7235-2477-4923-add8-f0c8ac8195c2">MMTIME</a> structure.
          


## -returns



If successful, returns <b>TIMERR_NOERROR</b>. Otherwise, returns an error code.




## -remarks



The system time is returned in the <b>ms</b> member of the <a href="https://msdn.microsoft.com/94bb7235-2477-4923-add8-f0c8ac8195c2">MMTIME</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/71680295-7fd3-4a8b-a574-78ea05e1d11d">Multimedia Timer Functions</a>



<a href="https://msdn.microsoft.com/25e0b313-64ff-4f30-ae0a-ac364ce3f0cf">Multimedia Timers</a>
 

 

