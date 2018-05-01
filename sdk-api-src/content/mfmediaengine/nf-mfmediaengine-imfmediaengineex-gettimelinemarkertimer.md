---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetTimelineMarkerTimer
title: IMFMediaEngineEx::GetTimelineMarkerTimer method
author: windows-driver-content
description: Gets the time of the next timeline marker, if any.
old-location: mf\imfmediaengineex_gettimelinemarkertimer.htm
old-project: medfound
ms.assetid: 8C58DBB6-A55E-4992-B4F2-EB36E15FA7A1
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: GetTimelineMarkerTimer method [Media Foundation], GetTimelineMarkerTimer method [Media Foundation], IMFMediaEngineEx interface, GetTimelineMarkerTimer,IMFMediaEngineEx.GetTimelineMarkerTimer, IMFMediaEngineEx, IMFMediaEngineEx interface [Media Foundation], GetTimelineMarkerTimer method, IMFMediaEngineEx::GetTimelineMarkerTimer, mf.imfmediaengineex_gettimelinemarkertimer, mfmediaengine/IMFMediaEngineEx::GetTimelineMarkerTimer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngineEx.GetTimelineMarkerTimer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineEx::GetTimelineMarkerTimer method


## -description


Gets the time of the next timeline marker, if any.


## -parameters




### -param pTimeToFire [out]

Receives the marker time, in seconds. If no marker is set, this parameter receives the value <b>NaN</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

