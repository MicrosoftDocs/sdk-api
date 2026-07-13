---
UID: NF:mpegtype.IMpegAudioDecoder.put_IntegerDecode
title: IMpegAudioDecoder::put_IntegerDecode (mpegtype.h)
description: Specifies whether the decoder will use integer-based decoding.
helpviewer_keywords: ["IMpegAudioDecoder interface [DirectShow]","put_IntegerDecode method","IMpegAudioDecoder.put_IntegerDecode","IMpegAudioDecoder::put_IntegerDecode","IMpegAudioDecoderputIntegerDecode","dshow.impegaudiodecoder_put_integerdecode","mpegtype/IMpegAudioDecoder::put_IntegerDecode","put_IntegerDecode","put_IntegerDecode method [DirectShow]","put_IntegerDecode method [DirectShow]","IMpegAudioDecoder interface"]
old-location: dshow\impegaudiodecoder_put_integerdecode.htm
tech.root: dshow
ms.assetid: a92fbcbf-0cd5-4c7a-bcde-a616a7d022bd
ms.date: 4/26/2023
ms.keywords: IMpegAudioDecoder interface [DirectShow],put_IntegerDecode method, IMpegAudioDecoder.put_IntegerDecode, IMpegAudioDecoder::put_IntegerDecode, IMpegAudioDecoderputIntegerDecode, dshow.impegaudiodecoder_put_integerdecode, mpegtype/IMpegAudioDecoder::put_IntegerDecode, put_IntegerDecode, put_IntegerDecode method [DirectShow], put_IntegerDecode method [DirectShow],IMpegAudioDecoder interface
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
 - IMpegAudioDecoder::put_IntegerDecode
 - mpegtype/IMpegAudioDecoder::put_IntegerDecode
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
 - IMpegAudioDecoder.put_IntegerDecode
---

# IMpegAudioDecoder::put_IntegerDecode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies whether the decoder will use integer-based decoding.

## -parameters

### -param IntDecode [in]

Specifies the decoding mode. 0 = floating point mode and 1 = integer mode.

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

## -see-also

<a href="/windows/desktop/api/mpegtype/nn-mpegtype-impegaudiodecoder">IMpegAudioDecoder</a>