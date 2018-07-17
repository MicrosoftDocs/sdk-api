---
UID: NF:mpegtype.IMpegAudioDecoder.put_DecoderAccuracy
title: IMpegAudioDecoder::put_DecoderAccuracy
author: windows-sdk-content
description: Specifies the decoder accuracy as a three-level quality setting.
old-location: dshow\impegaudiodecoder_put_decoderaccuracy.htm
old-project: DirectShow
ms.assetid: 1fcacbbc-a3e4-4c7b-a9d0-1ecf6a3dca07
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IMpegAudioDecoder interface [DirectShow],put_DecoderAccuracy method, IMpegAudioDecoder.put_DecoderAccuracy, IMpegAudioDecoder::put_DecoderAccuracy, IMpegAudioDecoderputDecoderAccuracy, dshow.impegaudiodecoder_put_decoderaccuracy, mpegtype/IMpegAudioDecoder::put_DecoderAccuracy, put_DecoderAccuracy, put_DecoderAccuracy method [DirectShow], put_DecoderAccuracy method [DirectShow],IMpegAudioDecoder interface
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
tech.root: 
req.typenames: MPEG_CONTEXT, *PMPEG_CONTEXT
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMpegAudioDecoder::put_DecoderAccuracy


## -description



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




<a href="https://msdn.microsoft.com/59fd96ef-2f9a-4a8e-bd08-2695de52b1c6">IMpegAudioDecoder</a>
 

 

