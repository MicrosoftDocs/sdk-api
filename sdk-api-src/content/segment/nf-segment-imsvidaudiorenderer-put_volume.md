---
UID: NF:segment.IMSVidAudioRenderer.put_Volume
title: IMSVidAudioRenderer::put_Volume (segment.h)
description: The put_Volume method specifies the audio renderer's volume level.helpviewer_keywords: ["IMSVidAudioRenderer interface [Microsoft TV Technologies]","put_Volume method","IMSVidAudioRenderer.put_Volume","IMSVidAudioRenderer::put_Volume","IMSVidAudioRendererput_Volume","mstv.imsvidaudiorenderer_put_volume","put_Volume","put_Volume method [Microsoft TV Technologies]","put_Volume method [Microsoft TV Technologies]","IMSVidAudioRenderer interface","segment/IMSVidAudioRenderer::put_Volume"]
old-location: mstv\imsvidaudiorenderer_put_volume.htm
tech.root: mstv
ms.assetid: a0fa96bb-a903-41e1-bd2a-6ef1733adbd4
ms.date: 12/05/2018
ms.keywords: IMSVidAudioRenderer interface [Microsoft TV Technologies],put_Volume method, IMSVidAudioRenderer.put_Volume, IMSVidAudioRenderer::put_Volume, IMSVidAudioRendererput_Volume, mstv.imsvidaudiorenderer_put_volume, put_Volume, put_Volume method [Microsoft TV Technologies], put_Volume method [Microsoft TV Technologies],IMSVidAudioRenderer interface, segment/IMSVidAudioRenderer::put_Volume
f1_keywords:
- segment/IMSVidAudioRenderer.put_Volume
dev_langs:
- c++
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
- IMSVidAudioRenderer.put_Volume
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicaudio-put_volume">IBasicAudio::put_Volume</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidaudiorenderer">IMSVidAudioRenderer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidaudiorenderer-get_volume">IMSVidAudioRenderer::get_Volume</a>
 

 

