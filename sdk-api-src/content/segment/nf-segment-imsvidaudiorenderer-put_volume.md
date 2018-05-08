---
UID: NF:segment.IMSVidAudioRenderer.put_Volume
title: IMSVidAudioRenderer::put_Volume
author: windows-driver-content
description: The put_Volume method specifies the audio renderer's volume level.
old-location: mstv\imsvidaudiorenderer_put_volume.htm
old-project: mstv
ms.assetid: a0fa96bb-a903-41e1-bd2a-6ef1733adbd4
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidAudioRenderer interface [Microsoft TV Technologies],put_Volume method, IMSVidAudioRenderer.put_Volume, IMSVidAudioRenderer::put_Volume, IMSVidAudioRendererput_Volume, mstv.imsvidaudiorenderer_put_volume, put_Volume, put_Volume method [Microsoft TV Technologies], put_Volume method [Microsoft TV Technologies],IMSVidAudioRenderer interface, segment/IMSVidAudioRenderer::put_Volume
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidAudioRenderer.put_Volume
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

