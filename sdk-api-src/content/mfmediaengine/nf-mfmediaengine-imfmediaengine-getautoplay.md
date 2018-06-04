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

# IMFMediaEngine::GetAutoPlay


## -description


Queries whether the Media Engine automatically begins playback.


## -parameters






## -returns



Returns <b>TRUE</b> if the Media Engine automatically begins playback, or <b>FALSE</b> otherwise.




## -remarks



This method corresponds to the <b>autoplay</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

If this method returns <b>TRUE</b>, playback begins automatically after the <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">IMFMediaEngine::Load</a> method completes. Otherwise, playback begins when the application calls <a href="https://msdn.microsoft.com/2D6083F5-734A-4350-8E54-56C79038389D">IMFMediaEngine::Play</a>.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>



<a href="https://msdn.microsoft.com/867FE1D2-39AE-4A44-99DD-98A8ABD234A2">IMFMediaEngine::SetAutoPlay</a>
 

 

