---
UID: NF:strmif.IAMAudioInputMixer.get_Bass
title: IAMAudioInputMixer::get_Bass (strmif.h)
description: The get_Bass method retrieves the bass equalization.
helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","get_Bass method","IAMAudioInputMixer.get_Bass","IAMAudioInputMixer::get_Bass","IAMAudioInputMixerget_Bass","dshow.iamaudioinputmixer_get_bass","get_Bass","get_Bass method [DirectShow]","get_Bass method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::get_Bass"]
old-location: dshow\iamaudioinputmixer_get_bass.htm
tech.root: dshow
ms.assetid: 08edf6be-81b7-4402-a500-1b7d9c389042
ms.date: 4/26/2023
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_Bass method, IAMAudioInputMixer.get_Bass, IAMAudioInputMixer::get_Bass, IAMAudioInputMixerget_Bass, dshow.iamaudioinputmixer_get_bass, get_Bass, get_Bass method [DirectShow], get_Bass method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_Bass
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMAudioInputMixer::get_Bass
 - strmif/IAMAudioInputMixer::get_Bass
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMAudioInputMixer.get_Bass
---

# IAMAudioInputMixer::get_Bass


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Bass</code> method retrieves the bass equalization.

## -parameters

### -param pBass [out]

Receives the bass gain, in decibels. A negative value indicates attenuation.

## -returns

If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_bass">IAMAudioInputMixer::put_Bass</a>