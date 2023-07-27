---
UID: NF:mpegtype.IMpegAudioDecoder.get_DecoderWordSize
title: IMpegAudioDecoder::get_DecoderWordSize (mpegtype.h)
description: Returns the word size used to decode, either eight or 16 bit.
helpviewer_keywords: ["IMpegAudioDecoder interface [DirectShow]","get_DecoderWordSize method","IMpegAudioDecoder.get_DecoderWordSize","IMpegAudioDecoder::get_DecoderWordSize","IMpegAudioDecodergetDecoderWordSize","dshow.impegaudiodecoder_get_decoderwordsize","get_DecoderWordSize","get_DecoderWordSize method [DirectShow]","get_DecoderWordSize method [DirectShow]","IMpegAudioDecoder interface","mpegtype/IMpegAudioDecoder::get_DecoderWordSize"]
old-location: dshow\impegaudiodecoder_get_decoderwordsize.htm
tech.root: dshow
ms.assetid: 92528359-cdbf-4490-badd-1ad20643ec1a
ms.date: 4/26/2023
ms.keywords: IMpegAudioDecoder interface [DirectShow],get_DecoderWordSize method, IMpegAudioDecoder.get_DecoderWordSize, IMpegAudioDecoder::get_DecoderWordSize, IMpegAudioDecodergetDecoderWordSize, dshow.impegaudiodecoder_get_decoderwordsize, get_DecoderWordSize, get_DecoderWordSize method [DirectShow], get_DecoderWordSize method [DirectShow],IMpegAudioDecoder interface, mpegtype/IMpegAudioDecoder::get_DecoderWordSize
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
 - IMpegAudioDecoder::get_DecoderWordSize
 - mpegtype/IMpegAudioDecoder::get_DecoderWordSize
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
 - IMpegAudioDecoder.get_DecoderWordSize
---

# IMpegAudioDecoder::get_DecoderWordSize


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Returns the word size used to decode, either eight or 16 bit.

## -parameters

### -param pWordSize [out]

Indicates the word size; the value is either 8 or 16.

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