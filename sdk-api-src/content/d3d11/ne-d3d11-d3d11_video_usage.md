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

# D3D11_VIDEO_USAGE enumeration


## -description


Specifies the intended use for a video processor.


## -enum-fields




### -field D3D11_VIDEO_USAGE_PLAYBACK_NORMAL

Normal video playback. The graphics driver should expose a set of capabilities that are appropriate for real-time video playback.




### -field D3D11_VIDEO_USAGE_OPTIMAL_SPEED

Optimal speed. The graphics driver should expose a minimal set of capabilities that are optimized for performance.



Use this setting if you want better performance and can accept some reduction in video quality. For example, you might use this setting in power-saving mode or to play video thumbnails.




### -field D3D11_VIDEO_USAGE_OPTIMAL_QUALITY

Optimal quality. The grahics driver should expose its maximum set of capabilities.

Specify this setting to get the best video quality possible. It is appropriate for tasks such as video editing, when quality is more important than speed. It is not appropriate for real-time playback.




## -see-also




<a href="https://msdn.microsoft.com/A1649897-B368-4D03-9A08-630C8C59E44A">D3D11_VIDEO_PROCESSOR_CONTENT_DESC</a>



<a href="https://msdn.microsoft.com/40061AD1-BCD9-4170-A442-34B4C792BB55">Direct3D 11 Video Enumerations</a>
 

 

