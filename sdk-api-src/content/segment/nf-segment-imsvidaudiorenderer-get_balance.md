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

# IMSVidAudioRenderer::get_Balance


## -description




The <b>get_Balance</b> method retrieves the audio renderer's balance level.


## -parameters




### -param lBal






#### - plBal [out]

Pointer to a variable that receives the balance level.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The balance level is a value between –10,000 and 10,000, measured in hundredths of a decibel (dB). If the value is –10,000, the left channel is at full volume and the right channel is attenuated by 100 dB. If the value is 10,000, the right channel is at full volume and the left channel is attenuated by 100 dB. If the value is zero, both channels are at full volume.




## -see-also




<a href="https://msdn.microsoft.com/bb9796c5-0dd2-496a-b5b4-a6614d7770c1">IBasicAudio::get_Balance</a>



<a href="https://msdn.microsoft.com/f822b5a6-c88e-48c9-91f4-611a3f147fe0">IMSVidAudioRenderer Interface</a>



<a href="https://msdn.microsoft.com/25a9231a-d34a-4657-be0a-fcc979d1745d">IMSVidAudioRenderer::put_Balance</a>
 

 

