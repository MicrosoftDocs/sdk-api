---
UID: NF:segment.IMSVidAudioRenderer.put_Balance
title: IMSVidAudioRenderer::put_Balance (segment.h)
author: windows-sdk-content
description: The put_Balance method specifies the audio renderer's balance level.
old-location: mstv\imsvidaudiorenderer_put_balance.htm
tech.root: mstv
ms.assetid: 25a9231a-d34a-4657-be0a-fcc979d1745d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidAudioRenderer interface [Microsoft TV Technologies],put_Balance method, IMSVidAudioRenderer.put_Balance, IMSVidAudioRenderer::put_Balance, IMSVidAudioRendererput_Balance, mstv.imsvidaudiorenderer_put_balance, put_Balance, put_Balance method [Microsoft TV Technologies], put_Balance method [Microsoft TV Technologies],IMSVidAudioRenderer interface, segment/IMSVidAudioRenderer::put_Balance
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidAudioRenderer.put_Balance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Dd389537(v=VS.85).aspx">IBasicAudio::put_Balance</a>



<a href="https://msdn.microsoft.com/f822b5a6-c88e-48c9-91f4-611a3f147fe0">IMSVidAudioRenderer Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694462(v=VS.85).aspx">IMSVidAudioRenderer::get_Balance</a>
 

 

