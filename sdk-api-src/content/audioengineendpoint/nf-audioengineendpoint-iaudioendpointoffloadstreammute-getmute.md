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

# IAudioEndpointOffloadStreamMute::GetMute


## -description


The <b>GetMute</b> method retrieves the mute status of the offloaded audio stream.


## -parameters




### -param pbMuted [out]

Indicates whether or not the offloaded audio stream is muted. A value of<b>TRUE</b> indicates that the stream is muted, and a value of<b>FALSE</b> indicates that the stream is not muted.


## -returns



The <b>GetMute</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/F102CBB2-6751-416C-B59B-F91440583594">IAudioEndpointOffloadStreamMute</a>
 

 

