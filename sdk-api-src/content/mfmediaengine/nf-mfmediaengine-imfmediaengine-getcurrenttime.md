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

# IMFMediaEngine::GetCurrentTime


## -description


Gets the current playback position.


## -parameters






## -returns



Returns the playback position, in seconds.




## -remarks



This method corresponds to the <b>currentTime</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5. 

Note that after you call <a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>, the time returned by <b>GetCurrentTime</b> may not be precisely accurate. Apps that need a frame-accurate position value, such as media editors, should call <a href="https://msdn.microsoft.com/090B5B6F-E4D1-43D7-AD09-BA3008B48104">FrameStep</a> immediately after calling **Pause** before calling <b>GetCurrentTime</b>.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

