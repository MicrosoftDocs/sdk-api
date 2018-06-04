---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

