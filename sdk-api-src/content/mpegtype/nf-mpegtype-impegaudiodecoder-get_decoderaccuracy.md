---
UID: NF:mpegtype.IMpegAudioDecoder.get_DecoderAccuracy
title: IMpegAudioDecoder::get_DecoderAccuracy (mpegtype.h)
description: Returns the decoder accuracy as a three-level quality setting.
helpviewer_keywords: ["IMpegAudioDecoder interface [DirectShow]","get_DecoderAccuracy method","IMpegAudioDecoder.get_DecoderAccuracy","IMpegAudioDecoder::get_DecoderAccuracy","IMpegAudioDecodergetDecoderAccuracy","dshow.impegaudiodecoder_get_decoderaccuracy","get_DecoderAccuracy","get_DecoderAccuracy method [DirectShow]","get_DecoderAccuracy method [DirectShow]","IMpegAudioDecoder interface","mpegtype/IMpegAudioDecoder::get_DecoderAccuracy"]
old-location: dshow\impegaudiodecoder_get_decoderaccuracy.htm
tech.root: dshow
ms.assetid: 5b0776f2-4340-4ebc-9d28-a2a2c2a4571e
ms.date: 12/05/2018
ms.keywords: IMpegAudioDecoder interface [DirectShow],get_DecoderAccuracy method, IMpegAudioDecoder.get_DecoderAccuracy, IMpegAudioDecoder::get_DecoderAccuracy, IMpegAudioDecodergetDecoderAccuracy, dshow.impegaudiodecoder_get_decoderaccuracy, get_DecoderAccuracy, get_DecoderAccuracy method [DirectShow], get_DecoderAccuracy method [DirectShow],IMpegAudioDecoder interface, mpegtype/IMpegAudioDecoder::get_DecoderAccuracy
f1_keywords:
- mpegtype/IMpegAudioDecoder.get_DecoderAccuracy
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IMpegAudioDecoder.get_DecoderAccuracy
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMpegAudioDecoder::get_DecoderAccuracy


## -description



Returns the decoder accuracy as a three-level quality setting.




## -parameters




### -param pAccuracy [out]

Indicates the quality setting. 0 = best, 0x4000 = high, and 0x8000 = full.


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




<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nn-mpegtype-impegaudiodecoder">IMpegAudioDecoder</a>
 

 

