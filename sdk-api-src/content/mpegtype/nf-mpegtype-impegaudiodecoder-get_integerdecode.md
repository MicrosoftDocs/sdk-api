---
UID: NF:mpegtype.IMpegAudioDecoder.get_IntegerDecode
title: IMpegAudioDecoder::get_IntegerDecode
author: windows-sdk-content
description: Returns whether the decoder is currently using integer-based decoding as opposed to floating point decoding.
old-location: dshow\impegaudiodecoder_get_integerdecode.htm
old-project: DirectShow
ms.assetid: 3cb73c5a-8bca-4dc3-a48c-cac57f3d7fbf
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IMpegAudioDecoder interface [DirectShow],get_IntegerDecode method, IMpegAudioDecoder.get_IntegerDecode, IMpegAudioDecoder::get_IntegerDecode, IMpegAudioDecodergetIntegerDecode, dshow.impegaudiodecoder_get_integerdecode, get_IntegerDecode, get_IntegerDecode method [DirectShow], get_IntegerDecode method [DirectShow],IMpegAudioDecoder interface, mpegtype/IMpegAudioDecoder::get_IntegerDecode
ms.prod: windows
ms.technology: windows-sdk
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
-	IMpegAudioDecoder.get_IntegerDecode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMpegAudioDecoder::get_IntegerDecode


## -description



Returns whether the decoder is currently using integer-based decoding as opposed to floating point decoding.




## -parameters




### -param pIntDecode [out]

Indicates whether the decoder is using integer-based decoding. Zero means it is using floating point-based decoding and one means it is using integer-based decoding.


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
 

 

