---
UID: NF:mpegtype.IMpegAudioDecoder.get_Stereo
title: IMpegAudioDecoder::get_Stereo (mpegtype.h)
description: Returns whether the decoder is decoding the encoded stream into stereo or mono PCM.
helpviewer_keywords: ["IMpegAudioDecoder interface [DirectShow]","get_Stereo method","IMpegAudioDecoder.get_Stereo","IMpegAudioDecoder::get_Stereo","IMpegAudioDecodergetStereo","dshow.impegaudiodecoder_get_stereo","get_Stereo","get_Stereo method [DirectShow]","get_Stereo method [DirectShow]","IMpegAudioDecoder interface","mpegtype/IMpegAudioDecoder::get_Stereo"]
old-location: dshow\impegaudiodecoder_get_stereo.htm
tech.root: dshow
ms.assetid: fb2b4b26-7588-42fd-a915-c09d512cb152
ms.date: 4/26/2023
ms.keywords: IMpegAudioDecoder interface [DirectShow],get_Stereo method, IMpegAudioDecoder.get_Stereo, IMpegAudioDecoder::get_Stereo, IMpegAudioDecodergetStereo, dshow.impegaudiodecoder_get_stereo, get_Stereo, get_Stereo method [DirectShow], get_Stereo method [DirectShow],IMpegAudioDecoder interface, mpegtype/IMpegAudioDecoder::get_Stereo
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
 - IMpegAudioDecoder::get_Stereo
 - mpegtype/IMpegAudioDecoder::get_Stereo
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
 - IMpegAudioDecoder.get_Stereo
---

# IMpegAudioDecoder::get_Stereo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Returns whether the decoder is decoding the encoded stream into stereo or mono PCM.

## -parameters

### -param pStereo [out]

Indicates whether the decoder is outputting to PCM mono or stereo.

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