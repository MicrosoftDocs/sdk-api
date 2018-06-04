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

# IMSVidAudioRenderer::get_Volume


## -description


The <b>get_Volume</b> method retrieves the audio renderer's volume level.


## -parameters




### -param lVol






#### - plVol [out]


            Pointer to a variable that receives the volume level, in units of .01 decibel (dB).
          


## -returns




            If the method succeeds, it returns S_OK. If it fails, it returns an error code.
          




## -remarks



Full volume is 0 and silence is –10,000. Divide by 100 to get the equivalent decibel value; for example, –10,000 is –100 dB.




## -see-also




<a href="https://msdn.microsoft.com/3258da5a-ab44-4c8a-813b-79a0c28693a3">IBasicAudio::get_Volume</a>



<a href="https://msdn.microsoft.com/f822b5a6-c88e-48c9-91f4-611a3f147fe0">IMSVidAudioRenderer Interface</a>



<a href="https://msdn.microsoft.com/a0fa96bb-a903-41e1-bd2a-6ef1733adbd4">IMSVidAudioRenderer::put_Volume</a>
 

 

