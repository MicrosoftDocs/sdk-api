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

# IMSVidPlaybackEvent::EndOfMedia


## -description



This topic applies to Windows XP or later.
        



The <b>EndOfMedia</b> method is called when playback reaches the end of the source media.


## -parameters




### -param lpd [in]

Specifies a pointer to the <a href="https://msdn.microsoft.com/ed954545-f58f-4841-9ffd-185350f76388">IMSVidPlayback</a> interface of the playback device.


## -returns



Return S_OK or an error code.




## -remarks



The dispatch identifier (dispid) of this method is <b>eventidEndOfMedia</b>.




## -see-also




<a href="https://msdn.microsoft.com/7347601e-e889-4a45-8b94-081678df68d9">IMSVidPlaybackEvent Interface</a>
 

 

