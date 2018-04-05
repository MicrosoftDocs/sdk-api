---
UID: NF:mpegtype.IMpegAudioDecoder.get_DecoderAccuracy
title: IMpegAudioDecoder::get_DecoderAccuracy method
author: windows-driver-content
description: Returns the decoder accuracy as a three-level quality setting.
old-location: dshow\impegaudiodecoder_get_decoderaccuracy.htm
old-project: DirectShow
ms.assetid: 5b0776f2-4340-4ebc-9d28-a2a2c2a4571e
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IMpegAudioDecoder, IMpegAudioDecoder interface [DirectShow], get_DecoderAccuracy method, IMpegAudioDecoder::get_DecoderAccuracy, IMpegAudioDecodergetDecoderAccuracy, dshow.impegaudiodecoder_get_decoderaccuracy, get_DecoderAccuracy method [DirectShow], get_DecoderAccuracy method [DirectShow], IMpegAudioDecoder interface, get_DecoderAccuracy,IMpegAudioDecoder.get_DecoderAccuracy, mpegtype/IMpegAudioDecoder::get_DecoderAccuracy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MPEG_CONTEXT, *PMPEG_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMpegAudioDecoder.get_DecoderAccuracy
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMpegAudioDecoder::get_DecoderAccuracy method


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




<a href="https://msdn.microsoft.com/59fd96ef-2f9a-4a8e-bd08-2695de52b1c6">IMpegAudioDecoder</a>
 

 

