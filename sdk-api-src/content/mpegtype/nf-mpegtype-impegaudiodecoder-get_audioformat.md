---
UID: NF:mpegtype.IMpegAudioDecoder.get_AudioFormat
title: IMpegAudioDecoder::get_AudioFormat (mpegtype.h)
description: Returns the audio format of the connected input pin.
helpviewer_keywords: ["IMpegAudioDecoder interface [DirectShow]","get_AudioFormat method","IMpegAudioDecoder.get_AudioFormat","IMpegAudioDecoder::get_AudioFormat","IMpegAudioDecodergetAudioFormat","dshow.impegaudiodecoder_get_audioformat","get_AudioFormat","get_AudioFormat method [DirectShow]","get_AudioFormat method [DirectShow]","IMpegAudioDecoder interface","mpegtype/IMpegAudioDecoder::get_AudioFormat"]
old-location: dshow\impegaudiodecoder_get_audioformat.htm
tech.root: dshow
ms.assetid: f7634504-d3f5-46a9-be25-08293190c27b
ms.date: 12/05/2018
ms.keywords: IMpegAudioDecoder interface [DirectShow],get_AudioFormat method, IMpegAudioDecoder.get_AudioFormat, IMpegAudioDecoder::get_AudioFormat, IMpegAudioDecodergetAudioFormat, dshow.impegaudiodecoder_get_audioformat, get_AudioFormat, get_AudioFormat method [DirectShow], get_AudioFormat method [DirectShow],IMpegAudioDecoder interface, mpegtype/IMpegAudioDecoder::get_AudioFormat
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
 - IMpegAudioDecoder::get_AudioFormat
 - mpegtype/IMpegAudioDecoder::get_AudioFormat
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
 - IMpegAudioDecoder.get_AudioFormat
---

# IMpegAudioDecoder::get_AudioFormat


## -description

Returns the audio format of the connected input pin.

## -parameters

### -param lpFmt [out]

Pointer to an <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat">MPEG1WAVEFORMAT</a> structure. The method copies the format data into the structure.

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