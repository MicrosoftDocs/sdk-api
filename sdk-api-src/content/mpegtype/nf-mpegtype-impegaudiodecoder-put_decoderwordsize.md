---
UID: NF:mpegtype.IMpegAudioDecoder.put_DecoderWordSize
title: IMpegAudioDecoder::put_DecoderWordSize
author: windows-sdk-content
description: Specifies the word size used by the decoder.
old-location: dshow\impegaudiodecoder_put_decoderwordsize.htm
old-project: DirectShow
ms.assetid: bd5ea824-5ac7-44e3-b7db-636e1b350d4e
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IMpegAudioDecoder interface [DirectShow],put_DecoderWordSize method, IMpegAudioDecoder.put_DecoderWordSize, IMpegAudioDecoder::put_DecoderWordSize, IMpegAudioDecoderputDecoderWordSize, dshow.impegaudiodecoder_put_decoderwordsize, mpegtype/IMpegAudioDecoder::put_DecoderWordSize, put_DecoderWordSize, put_DecoderWordSize method [DirectShow], put_DecoderWordSize method [DirectShow],IMpegAudioDecoder interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mpegtype.h
req.include-header: 
req.redist: 
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
 - IMpegAudioDecoder.put_DecoderWordSize
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMpegAudioDecoder::put_DecoderWordSize


## -description



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




<a href="https://msdn.microsoft.com/59fd96ef-2f9a-4a8e-bd08-2695de52b1c6">IMpegAudioDecoder</a>
 

 

