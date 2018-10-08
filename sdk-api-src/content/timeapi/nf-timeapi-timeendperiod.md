---
UID: NF:timeapi.timeEndPeriod
title: timeEndPeriod function
author: windows-sdk-content
description: The timeEndPeriod function clears a previously set minimum timer resolution.
old-location: multimedia\timeendperiod.htm
tech.root: Multimedia
ms.assetid: b06531f9-4fd7-4051-80d4-5a175fdd37e7
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "_win32_timeEndPeriod, mmsystem/timeEndPeriod, multimedia.timeendperiod, timeEndPeriod, timeEndPeriod function [Windows Multimedia], timeapi/timeEndPeriod"
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
 - timeEndPeriod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# timeEndPeriod function


## -description



The <b>timeEndPeriod</b> function clears a previously set minimum timer resolution.




## -parameters




### -param uPeriod

Minimum timer resolution specified in the previous call to the <a href="https://msdn.microsoft.com/7168981c-9af8-4665-88a2-7d96a8f2b273">timeBeginPeriod</a> function.


## -returns



Returns <b>TIMERR_NOERROR</b> if successful or <b>TIMERR_NOCANDO</b> if the resolution specified in uPeriod is out of range.




## -remarks



Call this function immediately after you are finished using timer services.

You must match each call to <a href="https://msdn.microsoft.com/7168981c-9af8-4665-88a2-7d96a8f2b273">timeBeginPeriod</a> with a call to <b>timeEndPeriod</b>, specifying the same minimum resolution in both calls. An application can make multiple <b>timeBeginPeriod</b> calls as long as each call is matched with a call to <b>timeEndPeriod</b>.




## -see-also




<a href="https://msdn.microsoft.com/71680295-7fd3-4a8b-a574-78ea05e1d11d">Multimedia Timer Functions</a>



<a href="https://msdn.microsoft.com/25e0b313-64ff-4f30-ae0a-ac364ce3f0cf">Multimedia Timers</a>
 

 

