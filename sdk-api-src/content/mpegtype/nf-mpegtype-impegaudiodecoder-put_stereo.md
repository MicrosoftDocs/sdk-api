---
UID: NF:mpegtype.IMpegAudioDecoder.put_Stereo
title: IMpegAudioDecoder::put_Stereo
author: windows-sdk-content
description: Specifies whether the decoder will decode the encoded stream into stereo or mono PCM.
old-location: dshow\impegaudiodecoder_put_stereo.htm
old-project: DirectShow
ms.assetid: 238e33ba-f35c-423c-be5f-73d1ca14cebd
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IMpegAudioDecoder interface [DirectShow],put_Stereo method, IMpegAudioDecoder.put_Stereo, IMpegAudioDecoder::put_Stereo, IMpegAudioDecoderputStereo, dshow.impegaudiodecoder_put_stereo, mpegtype/IMpegAudioDecoder::put_Stereo, put_Stereo, put_Stereo method [DirectShow], put_Stereo method [DirectShow],IMpegAudioDecoder interface
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
 - IMpegAudioDecoder.put_Stereo
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMpegAudioDecoder::put_Stereo


## -description



Specifies whether the decoder will decode the encoded stream into stereo or mono PCM.




## -parameters




### -param Stereo [in]

Specifies the decoded output type. 1 = mono and 2 = stereo.


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
 

 

