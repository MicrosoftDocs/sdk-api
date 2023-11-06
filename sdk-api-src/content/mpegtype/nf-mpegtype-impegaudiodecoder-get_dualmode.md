---
UID: NF:mpegtype.IMpegAudioDecoder.get_DualMode
title: IMpegAudioDecoder::get_DualMode (mpegtype.h)
description: Returns which channel is currently being decoded.
helpviewer_keywords: ["IMpegAudioDecoder interface [DirectShow]","get_DualMode method","IMpegAudioDecoder.get_DualMode","IMpegAudioDecoder::get_DualMode","IMpegAudioDecodergetDualMode","dshow.impegaudiodecoder_get_dualmode","get_DualMode","get_DualMode method [DirectShow]","get_DualMode method [DirectShow]","IMpegAudioDecoder interface","mpegtype/IMpegAudioDecoder::get_DualMode"]
old-location: dshow\impegaudiodecoder_get_dualmode.htm
tech.root: dshow
ms.assetid: 3b536e8c-91eb-4c32-955f-b343f2c8e16f
ms.date: 4/26/2023
ms.keywords: IMpegAudioDecoder interface [DirectShow],get_DualMode method, IMpegAudioDecoder.get_DualMode, IMpegAudioDecoder::get_DualMode, IMpegAudioDecodergetDualMode, dshow.impegaudiodecoder_get_dualmode, get_DualMode, get_DualMode method [DirectShow], get_DualMode method [DirectShow],IMpegAudioDecoder interface, mpegtype/IMpegAudioDecoder::get_DualMode
req.header: mpegtype.h
req.include-header: 
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
 - IMpegAudioDecoder::get_DualMode
 - mpegtype/IMpegAudioDecoder::get_DualMode
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
 - IMpegAudioDecoder.get_DualMode
---

# IMpegAudioDecoder::get_DualMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Returns which channel is currently being decoded.

## -parameters

### -param pIntDecode [out]

Indicates the channel(s) to be decoded.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

The <i>pIntDecode</i> parameter can have one of the values in the following table.

<table>
<tr>
<th>Constant
            </th>
<th>Description
            </th>
</tr>
<tr>
<td><b>AM_MPEG_AUDIO_DUAL_MERGE
            </b></td>
<td>Both channels are decoded.</td>
</tr>
<tr>
<td><b>AM_MPEG_AUDIO_DUAL_LEFT
            </b></td>
<td>The left channel is decoded.</td>
</tr>
<tr>
<td><b>AM_MPEG_AUDIO_DUAL_RIGHT
            </b></td>
<td>The right channel is decoded.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mpegtype/nn-mpegtype-impegaudiodecoder">IMpegAudioDecoder</a>