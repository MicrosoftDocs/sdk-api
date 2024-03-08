---
UID: NF:mpegtype.IMpegAudioDecoder.put_DecoderWordSize
title: IMpegAudioDecoder::put_DecoderWordSize (mpegtype.h)
description: Specifies the word size used by the decoder.
helpviewer_keywords: ["IMpegAudioDecoder interface [DirectShow]","put_DecoderWordSize method","IMpegAudioDecoder.put_DecoderWordSize","IMpegAudioDecoder::put_DecoderWordSize","IMpegAudioDecoderputDecoderWordSize","dshow.impegaudiodecoder_put_decoderwordsize","mpegtype/IMpegAudioDecoder::put_DecoderWordSize","put_DecoderWordSize","put_DecoderWordSize method [DirectShow]","put_DecoderWordSize method [DirectShow]","IMpegAudioDecoder interface"]
old-location: dshow\impegaudiodecoder_put_decoderwordsize.htm
tech.root: dshow
ms.assetid: bd5ea824-5ac7-44e3-b7db-636e1b350d4e
ms.date: 4/26/2023
ms.keywords: IMpegAudioDecoder interface [DirectShow],put_DecoderWordSize method, IMpegAudioDecoder.put_DecoderWordSize, IMpegAudioDecoder::put_DecoderWordSize, IMpegAudioDecoderputDecoderWordSize, dshow.impegaudiodecoder_put_decoderwordsize, mpegtype/IMpegAudioDecoder::put_DecoderWordSize, put_DecoderWordSize, put_DecoderWordSize method [DirectShow], put_DecoderWordSize method [DirectShow],IMpegAudioDecoder interface
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
 - IMpegAudioDecoder::put_DecoderWordSize
 - mpegtype/IMpegAudioDecoder::put_DecoderWordSize
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
 - IMpegAudioDecoder.put_DecoderWordSize
---

# IMpegAudioDecoder::put_DecoderWordSize


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the word size used by the decoder.

## -parameters

### -param WordSize [in]

Specifies the word size; value must be 8 or 16.

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