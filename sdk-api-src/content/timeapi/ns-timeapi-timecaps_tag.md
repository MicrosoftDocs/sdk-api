---
UID: NS:timeapi.timecaps_tag
title: timecaps_tag
author: windows-sdk-content
description: The TIMECAPS structure contains information about the resolution of the timer.
old-location: multimedia\timecaps.htm
tech.root: Multimedia
ms.assetid: 64a5c4ba-d340-4abc-8da3-766f3a2d7ec8
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "*LPTIMECAPS, *NPTIMECAPS, *PTIMECAPS, LPTIMECAPS, LPTIMECAPS structure pointer [Windows Multimedia], NPTIMECAPS, NPTIMECAPS structure pointer [Windows Multimedia], PTIMECAPS, PTIMECAPS structure pointer [Windows Multimedia], TIMECAPS, TIMECAPS structure [Windows Multimedia], _win32_TIMECAPS_str, mmsystem/LPTIMECAPS, mmsystem/NPTIMECAPS, mmsystem/PTIMECAPS, mmsystem/TIMECAPS, multimedia.timecaps, timeapi/LPTIMECAPS, timeapi/NPTIMECAPS, timeapi/PTIMECAPS, timeapi/TIMECAPS, timecaps_tag"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: TIMECAPS, *PTIMECAPS, *NPTIMECAPS, *LPTIMECAPS
req.redist: 
---

# timecaps_tag structure


## -description


The <b>TIMECAPS</b> structure contains information about the resolution of the timer.


## -struct-fields




### -field wPeriodMin

The minimum supported resolution, in milliseconds.


### -field wPeriodMax

The maximum supported resolution, in milliseconds.


## -see-also




<a href="https://msdn.microsoft.com/202c27be-01d5-4381-b71a-7a3f4e4c7adf">Multimedia Timer Structures</a>



<a href="https://msdn.microsoft.com/25e0b313-64ff-4f30-ae0a-ac364ce3f0cf">Multimedia Timers</a>



<a href="https://msdn.microsoft.com/2e5e94fe-8175-417f-8c59-9d5cf052ea89">Timer Resolution</a>



<a href="https://msdn.microsoft.com/7b5a9675-1152-4c9e-bc79-fe9afa5c563c">timeGetDevCaps</a>
 

 

