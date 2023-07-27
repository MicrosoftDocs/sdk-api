---
UID: NF:mpegtype.IMpegAudioDecoder.put_DecoderAccuracy
title: IMpegAudioDecoder::put_DecoderAccuracy (mpegtype.h)
description: Specifies the decoder accuracy as a three-level quality setting.
helpviewer_keywords: ["IMpegAudioDecoder interface [DirectShow]","put_DecoderAccuracy method","IMpegAudioDecoder.put_DecoderAccuracy","IMpegAudioDecoder::put_DecoderAccuracy","IMpegAudioDecoderputDecoderAccuracy","dshow.impegaudiodecoder_put_decoderaccuracy","mpegtype/IMpegAudioDecoder::put_DecoderAccuracy","put_DecoderAccuracy","put_DecoderAccuracy method [DirectShow]","put_DecoderAccuracy method [DirectShow]","IMpegAudioDecoder interface"]
old-location: dshow\impegaudiodecoder_put_decoderaccuracy.htm
tech.root: dshow
ms.assetid: 1fcacbbc-a3e4-4c7b-a9d0-1ecf6a3dca07
ms.date: 4/26/2023
ms.keywords: IMpegAudioDecoder interface [DirectShow],put_DecoderAccuracy method, IMpegAudioDecoder.put_DecoderAccuracy, IMpegAudioDecoder::put_DecoderAccuracy, IMpegAudioDecoderputDecoderAccuracy, dshow.impegaudiodecoder_put_decoderaccuracy, mpegtype/IMpegAudioDecoder::put_DecoderAccuracy, put_DecoderAccuracy, put_DecoderAccuracy method [DirectShow], put_DecoderAccuracy method [DirectShow],IMpegAudioDecoder interface
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
 - IMpegAudioDecoder::put_DecoderAccuracy
 - mpegtype/IMpegAudioDecoder::put_DecoderAccuracy
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
 - IMpegAudioDecoder.put_DecoderAccuracy
---

# IMpegAudioDecoder::put_DecoderAccuracy


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the decoder accuracy as a three-level quality setting.

## -parameters

### -param Accuracy [in]

Indicates the quality setting. 0 = best, 0x4000 = high, 0x8000 = full.

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