---
UID: NF:mpegtype.IMpegAudioDecoder.put_DualMode
title: IMpegAudioDecoder::put_DualMode (mpegtype.h)
description: Specifies the channel to be decoded.
helpviewer_keywords: ["IMpegAudioDecoder interface [DirectShow]","put_DualMode method","IMpegAudioDecoder.put_DualMode","IMpegAudioDecoder::put_DualMode","IMpegAudioDecoderputDualMode","dshow.impegaudiodecoder_put_dualmode","mpegtype/IMpegAudioDecoder::put_DualMode","put_DualMode","put_DualMode method [DirectShow]","put_DualMode method [DirectShow]","IMpegAudioDecoder interface"]
old-location: dshow\impegaudiodecoder_put_dualmode.htm
tech.root: dshow
ms.assetid: b183f669-14bf-44d4-a17d-09cbc593309d
ms.date: 12/05/2018
ms.keywords: IMpegAudioDecoder interface [DirectShow],put_DualMode method, IMpegAudioDecoder.put_DualMode, IMpegAudioDecoder::put_DualMode, IMpegAudioDecoderputDualMode, dshow.impegaudiodecoder_put_dualmode, mpegtype/IMpegAudioDecoder::put_DualMode, put_DualMode, put_DualMode method [DirectShow], put_DualMode method [DirectShow],IMpegAudioDecoder interface
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
 - IMpegAudioDecoder::put_DualMode
 - mpegtype/IMpegAudioDecoder::put_DualMode
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
 - IMpegAudioDecoder.put_DualMode
---

# IMpegAudioDecoder::put_DualMode


## -description

Specifies the channel to be decoded.

## -parameters

### -param IntDecode [in]

Specifies the channel(s) to be decoded. See remarks for valid values.

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

The following table lists the valid values for the <i>pIntDecode</i> parameter.

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
<td>Specifies that both channels will be decoded.</td>
</tr>
<tr>
<td><b>AM_MPEG_AUDIO_DUAL_LEFT
            </b></td>
<td>Specifies that the left channel will be decoded.</td>
</tr>
<tr>
<td><b>AM_MPEG_AUDIO_DUAL_RIGHT
            </b></td>
<td>Specifies that the right channel will be decoded.</td>
</tr>
</table>
 

This method is useful for karaoke discs in Video CD (VCD) format that have two mono channels in the audio stream.

## -see-also

<a href="/windows/desktop/api/mpegtype/nn-mpegtype-impegaudiodecoder">IMpegAudioDecoder</a>