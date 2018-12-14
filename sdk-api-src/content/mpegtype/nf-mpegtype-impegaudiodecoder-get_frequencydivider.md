---
UID: NF:mpegtype.IMpegAudioDecoder.get_FrequencyDivider
title: IMpegAudioDecoder::get_FrequencyDivider
author: windows-sdk-content
description: Returns the frequency divider as a quality setting equal to CD Audio, FM Radio, or AM Radio.
old-location: dshow\impegaudiodecoder_get_frequencydivider.htm
tech.root: DirectShow
ms.assetid: 8b9b2a3f-2495-4da3-8a09-2ba31538bdb0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMpegAudioDecoder interface [DirectShow],get_FrequencyDivider method, IMpegAudioDecoder.get_FrequencyDivider, IMpegAudioDecoder::get_FrequencyDivider, IMpegAudioDecodergetFrequencyDivider, dshow.impegaudiodecoder_get_frequencydivider, get_FrequencyDivider, get_FrequencyDivider method [DirectShow], get_FrequencyDivider method [DirectShow],IMpegAudioDecoder interface, mpegtype/IMpegAudioDecoder::get_FrequencyDivider
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
 - IMpegAudioDecoder.get_FrequencyDivider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMpegAudioDecoder::get_FrequencyDivider


## -description



Returns the frequency divider as a quality setting equal to CD Audio, FM Radio, or AM Radio.




## -parameters




### -param pDivider [out]

Receives the frequency divider.
          


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




<a href="https://msdn.microsoft.com/en-us/library/Dd376656(v=VS.85).aspx">IMpegAudioDecoder</a>
 

 

