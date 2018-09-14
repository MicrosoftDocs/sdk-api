---
UID: NF:mfmediaengine.IMFMediaEngine.GetDefaultPlaybackRate
title: IMFMediaEngine::GetDefaultPlaybackRate
author: windows-sdk-content
description: Gets the default playback rate.
old-location: mf\imfmediaengine_getdefaultplaybackrate.htm
tech.root: medfound
ms.assetid: FF7E9E76-B85E-40BB-88BD-5033FCE31177
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: GetDefaultPlaybackRate, GetDefaultPlaybackRate method [Media Foundation], GetDefaultPlaybackRate method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetDefaultPlaybackRate method, IMFMediaEngine.GetDefaultPlaybackRate, IMFMediaEngine::GetDefaultPlaybackRate, mf.imfmediaengine_getdefaultplaybackrate, mfmediaengine/IMFMediaEngine::GetDefaultPlaybackRate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngine.GetDefaultPlaybackRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngine::GetDefaultPlaybackRate


## -description


Gets the default playback rate.


## -parameters






## -returns



Returns the default playback rate, as a multiple of normal (1×) playback. A negative value indicates reverse playback.




## -remarks



This method corresponds to getting the <b>defaultPlaybackRate</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5. 

The default playback rate is used for the next call to the <a href="https://msdn.microsoft.com/2D6083F5-734A-4350-8E54-56C79038389D">IMFMediaEngine::Play</a> method. To change the current playback rate, call <a href="https://msdn.microsoft.com/648BF1CC-BFAC-4874-808B-F8B46E3E9989">IMFMediaEngine::SetPlaybackRate</a>.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

