---
UID: NF:segment.IMSVidAudioRenderer.get_Balance
title: IMSVidAudioRenderer::get_Balance
author: windows-sdk-content
description: "."
old-location: mstv\imsvidaudiorenderer_get_balance.htm
old-project: mstv
ms.assetid: 59def393-ab3d-41a8-968a-cd22429874a0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidAudioRenderer interface [Microsoft TV Technologies],get_Balance method, IMSVidAudioRenderer.get_Balance, IMSVidAudioRenderer::get_Balance, IMSVidAudioRendererget_Balance, get_Balance, get_Balance method [Microsoft TV Technologies], get_Balance method [Microsoft TV Technologies],IMSVidAudioRenderer interface, mstv.imsvidaudiorenderer_get_balance, segment/IMSVidAudioRenderer::get_Balance
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidAudioRenderer.get_Balance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

