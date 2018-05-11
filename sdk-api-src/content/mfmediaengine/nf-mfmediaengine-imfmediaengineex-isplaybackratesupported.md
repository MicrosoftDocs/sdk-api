---
UID: NF:mfmediaengine.IMFMediaEngineEx.IsPlaybackRateSupported
title: IMFMediaEngineEx::IsPlaybackRateSupported
author: windows-driver-content
description: Queries whether the Media Engine can play at a specified playback rate.
old-location: mf\imfmediaengineex_isplaybackratesupported.htm
old-project: medfound
ms.assetid: 2BE9954A-0B67-45A8-9B79-1148DCB4DDC4
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],IsPlaybackRateSupported method, IMFMediaEngineEx.IsPlaybackRateSupported, IMFMediaEngineEx::IsPlaybackRateSupported, IsPlaybackRateSupported, IsPlaybackRateSupported method [Media Foundation], IsPlaybackRateSupported method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_isplaybackratesupported, mfmediaengine/IMFMediaEngineEx::IsPlaybackRateSupported
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
-	IMFMediaEngineEx.IsPlaybackRateSupported
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineEx::IsPlaybackRateSupported


## -description


Queries whether the Media Engine can play at a specified playback rate.


## -parameters




### -param rate [in]

The requested playback rate.


## -returns



Returns <b>TRUE</b> if the playback rate is supported, or <b>FALSE</b> otherwise.




## -remarks



Playback rates are expressed as a ratio of the current rate to the normal rate. For example, 1.0 is normal playback speed, 0.5 is half speed, and 2.0 is 2× speed. Positive values mean forward playback, and negative values mean reverse playback.

The results of this method can vary depending on the media resource that is currently loaded. Some media formats might support faster playback rates than others. Also, some formats might not support reverse play.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

