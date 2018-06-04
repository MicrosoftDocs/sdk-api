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

# IMSVidAudioRenderer::put_Balance


## -description


The <b>put_Balance</b> method specifies the audio renderer's balance level.


## -parameters




### -param lBal [in]

Specifies the balance level.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The balance level is a value between –10,000 and 10,000, measured in hundredths of a decibel (dB). If the value is -10,000, the left channel is at full volume and the right channel is attenuated by 100 dB. If the value is 10,000, the right channel is at full volume and the left channel is attenuated by 100 dB. If the value is zero, both channels are at full volume.




## -see-also




<a href="https://msdn.microsoft.com/88cf4639-8f32-424f-a097-272c44592f6f">IBasicAudio::put_Balance</a>



<a href="https://msdn.microsoft.com/f822b5a6-c88e-48c9-91f4-611a3f147fe0">IMSVidAudioRenderer Interface</a>



<a href="https://msdn.microsoft.com/59def393-ab3d-41a8-968a-cd22429874a0">IMSVidAudioRenderer::get_Balance</a>
 

 

