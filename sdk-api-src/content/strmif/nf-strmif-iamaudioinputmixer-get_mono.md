---
UID: NF:strmif.IAMAudioInputMixer.get_Mono
title: IAMAudioInputMixer::get_Mono (strmif.h)
description: The get_Mono method queries whether all channels are combined into a mono signal.
helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","get_Mono method","IAMAudioInputMixer.get_Mono","IAMAudioInputMixer::get_Mono","IAMAudioInputMixerget_Mono","dshow.iamaudioinputmixer_get_mono","get_Mono","get_Mono method [DirectShow]","get_Mono method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::get_Mono"]
old-location: dshow\iamaudioinputmixer_get_mono.htm
tech.root: dshow
ms.assetid: 0c0ce59d-6083-4af2-856b-41a1c9d83295
ms.date: 4/26/2023
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_Mono method, IAMAudioInputMixer.get_Mono, IAMAudioInputMixer::get_Mono, IAMAudioInputMixerget_Mono, dshow.iamaudioinputmixer_get_mono, get_Mono, get_Mono method [DirectShow], get_Mono method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_Mono
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
 - IAMAudioInputMixer::get_Mono
 - strmif/IAMAudioInputMixer::get_Mono
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
 - IAMAudioInputMixer.get_Mono
---

# IAMAudioInputMixer::get_Mono


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Mono</code> method queries whether all channels are combined into a mono signal.

## -parameters

### -param pfMono [out]

Receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Mono</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Multichannel</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_mono">IAMAudioInputMixer::put_Mono</a>