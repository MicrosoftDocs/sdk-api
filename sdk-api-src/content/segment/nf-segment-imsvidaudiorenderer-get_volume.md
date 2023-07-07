---
UID: NF:segment.IMSVidAudioRenderer.get_Volume
title: IMSVidAudioRenderer::get_Volume (segment.h)
description: The get_Volume method retrieves the audio renderer's volume level.
helpviewer_keywords: ["IMSVidAudioRenderer interface [Microsoft TV Technologies]","get_Volume method","IMSVidAudioRenderer.get_Volume","IMSVidAudioRenderer::get_Volume","IMSVidAudioRendererget_Volume","get_Volume","get_Volume method [Microsoft TV Technologies]","get_Volume method [Microsoft TV Technologies]","IMSVidAudioRenderer interface","mstv.imsvidaudiorenderer_get_volume","segment/IMSVidAudioRenderer::get_Volume"]
old-location: mstv\imsvidaudiorenderer_get_volume.htm
tech.root: mstv
ms.assetid: 7dbbdb17-b077-4e36-a5d4-c8e343feb930
ms.date: 12/05/2018
ms.keywords: IMSVidAudioRenderer interface [Microsoft TV Technologies],get_Volume method, IMSVidAudioRenderer.get_Volume, IMSVidAudioRenderer::get_Volume, IMSVidAudioRendererget_Volume, get_Volume, get_Volume method [Microsoft TV Technologies], get_Volume method [Microsoft TV Technologies],IMSVidAudioRenderer interface, mstv.imsvidaudiorenderer_get_volume, segment/IMSVidAudioRenderer::get_Volume
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidAudioRenderer::get_Volume
 - segment/IMSVidAudioRenderer::get_Volume
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidAudioRenderer.get_Volume
---

# IMSVidAudioRenderer::get_Volume


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Volume</b> method retrieves the audio renderer's volume level.

## -parameters

### -param lVol [out]

Pointer to a variable that receives the volume level, in units of .01 decibel (dB).

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Full volume is 0 and silence is –10,000. Divide by 100 to get the equivalent decibel value; for example, –10,000 is –100 dB.

## -see-also

<a href="/windows/desktop/api/control/nf-control-ibasicaudio-get_volume">IBasicAudio::get_Volume</a>



<a href="/previous-versions/windows/desktop/mstv/msvidaudiorenderer">IMSVidAudioRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidaudiorenderer-put_volume">IMSVidAudioRenderer::put_Volume</a>