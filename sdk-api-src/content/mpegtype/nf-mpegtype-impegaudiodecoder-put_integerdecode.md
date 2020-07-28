---
UID: NF:mpegtype.IMpegAudioDecoder.put_IntegerDecode
title: IMpegAudioDecoder::put_IntegerDecode (mpegtype.h)
description: Specifies whether the decoder will use integer-based decoding.
helpviewer_keywords: ["IMpegAudioDecoder interface [DirectShow]","put_IntegerDecode method","IMpegAudioDecoder.put_IntegerDecode","IMpegAudioDecoder::put_IntegerDecode","IMpegAudioDecoderputIntegerDecode","dshow.impegaudiodecoder_put_integerdecode","mpegtype/IMpegAudioDecoder::put_IntegerDecode","put_IntegerDecode","put_IntegerDecode method [DirectShow]","put_IntegerDecode method [DirectShow]","IMpegAudioDecoder interface"]
old-location: dshow\impegaudiodecoder_put_integerdecode.htm
tech.root: dshow
ms.assetid: a92fbcbf-0cd5-4c7a-bcde-a616a7d022bd
ms.date: 12/05/2018
ms.keywords: IMpegAudioDecoder interface [DirectShow],put_IntegerDecode method, IMpegAudioDecoder.put_IntegerDecode, IMpegAudioDecoder::put_IntegerDecode, IMpegAudioDecoderputIntegerDecode, dshow.impegaudiodecoder_put_integerdecode, mpegtype/IMpegAudioDecoder::put_IntegerDecode, put_IntegerDecode, put_IntegerDecode method [DirectShow], put_IntegerDecode method [DirectShow],IMpegAudioDecoder interface
f1_keywords:
- mpegtype/IMpegAudioDecoder.put_IntegerDecode
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
- IMpegAudioDecoder.put_IntegerDecode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMpegAudioDecoder::put_IntegerDecode


## -description



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




<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nn-mpegtype-impegaudiodecoder">IMpegAudioDecoder</a>
 

 

