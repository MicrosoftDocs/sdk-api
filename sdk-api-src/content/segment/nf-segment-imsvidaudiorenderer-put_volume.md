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

# IMSVidAudioRenderer::put_Volume


## -description


The <b>put_Volume</b> method specifies the audio renderer's volume level.


## -parameters




### -param lVol [in]

Specifies the volume level, in units of .01 decibel (dB).


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Full volume is 0 and silence is –10,000. Multiply the desired decibel level by 100; for example, –100 dB is –10,000.




## -see-also




<a href="https://msdn.microsoft.com/95171b87-e558-450b-8a48-f43a19069218">IBasicAudio::put_Volume</a>



<a href="https://msdn.microsoft.com/f822b5a6-c88e-48c9-91f4-611a3f147fe0">IMSVidAudioRenderer Interface</a>



<a href="https://msdn.microsoft.com/7dbbdb17-b077-4e36-a5d4-c8e343feb930">IMSVidAudioRenderer::get_Volume</a>
 

 

