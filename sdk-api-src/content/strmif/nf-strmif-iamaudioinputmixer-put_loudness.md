---
UID: NF:strmif.IAMAudioInputMixer.put_Loudness
title: IAMAudioInputMixer::put_Loudness (strmif.h)
description: The put_Loudness method enables or disables the loudness control.
helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","put_Loudness method","IAMAudioInputMixer.put_Loudness","IAMAudioInputMixer::put_Loudness","IAMAudioInputMixerput_Loudness","dshow.iamaudioinputmixer_put_loudness","put_Loudness","put_Loudness method [DirectShow]","put_Loudness method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::put_Loudness"]
old-location: dshow\iamaudioinputmixer_put_loudness.htm
tech.root: dshow
ms.assetid: e4baca46-260c-45fe-8c03-304c906aab15
ms.date: 4/26/2023
ms.keywords: IAMAudioInputMixer interface [DirectShow],put_Loudness method, IAMAudioInputMixer.put_Loudness, IAMAudioInputMixer::put_Loudness, IAMAudioInputMixerput_Loudness, dshow.iamaudioinputmixer_put_loudness, put_Loudness, put_Loudness method [DirectShow], put_Loudness method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::put_Loudness
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
 - IAMAudioInputMixer::put_Loudness
 - strmif/IAMAudioInputMixer::put_Loudness
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
 - IAMAudioInputMixer.put_Loudness
---

# IAMAudioInputMixer::put_Loudness


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Loudness</code> method enables or disables the loudness control.

## -parameters

### -param fLoudness [in]

Specifies whether loudness is on or off. Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Sets loudness on.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Sets loudness off.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

Loudness boosts the bass of low volume signals before they are recorded, to compensate for the fact that the ear does not hear quiet bass sounds as well as other sounds.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_loudness">IAMAudioInputMixer::get_Loudness</a>