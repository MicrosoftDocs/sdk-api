---
UID: NF:strmif.IAMAudioInputMixer.get_Loudness
title: IAMAudioInputMixer::get_Loudness (strmif.h)
description: The get_Loudness method retrieves the loudness control setting.
helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","get_Loudness method","IAMAudioInputMixer.get_Loudness","IAMAudioInputMixer::get_Loudness","IAMAudioInputMixerget_Loudness","dshow.iamaudioinputmixer_get_loudness","get_Loudness","get_Loudness method [DirectShow]","get_Loudness method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::get_Loudness"]
old-location: dshow\iamaudioinputmixer_get_loudness.htm
tech.root: dshow
ms.assetid: 620003c0-401f-4415-a82f-a80e7b32dbd3
ms.date: 4/26/2023
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_Loudness method, IAMAudioInputMixer.get_Loudness, IAMAudioInputMixer::get_Loudness, IAMAudioInputMixerget_Loudness, dshow.iamaudioinputmixer_get_loudness, get_Loudness, get_Loudness method [DirectShow], get_Loudness method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_Loudness
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
 - IAMAudioInputMixer::get_Loudness
 - strmif/IAMAudioInputMixer::get_Loudness
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
 - IAMAudioInputMixer.get_Loudness
---

# IAMAudioInputMixer::get_Loudness


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Loudness</code> method retrieves the loudness control setting.

## -parameters

### -param pfLoudness [out]

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
<td>Loudness is on.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Loudness is off.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_loudness">IAMAudioInputMixer::put_Loudness</a>