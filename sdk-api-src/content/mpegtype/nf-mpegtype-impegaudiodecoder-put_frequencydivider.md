---
UID: NF:mpegtype.IMpegAudioDecoder.put_FrequencyDivider
title: IMpegAudioDecoder::put_FrequencyDivider (mpegtype.h)
description: Specifies the frequency divider as a three-level setting corresponding to the quality of CD Audio, FM Radio, or AM Radio.
helpviewer_keywords: ["IMpegAudioDecoder interface [DirectShow]","put_FrequencyDivider method","IMpegAudioDecoder.put_FrequencyDivider","IMpegAudioDecoder::put_FrequencyDivider","IMpegAudioDecoderputFrequencyDivider","dshow.impegaudiodecoder_put_frequencydivider","mpegtype/IMpegAudioDecoder::put_FrequencyDivider","put_FrequencyDivider","put_FrequencyDivider method [DirectShow]","put_FrequencyDivider method [DirectShow]","IMpegAudioDecoder interface"]
old-location: dshow\impegaudiodecoder_put_frequencydivider.htm
tech.root: dshow
ms.assetid: 96e5d8f3-b658-408d-a615-e681d8731442
ms.date: 12/05/2018
ms.keywords: IMpegAudioDecoder interface [DirectShow],put_FrequencyDivider method, IMpegAudioDecoder.put_FrequencyDivider, IMpegAudioDecoder::put_FrequencyDivider, IMpegAudioDecoderputFrequencyDivider, dshow.impegaudiodecoder_put_frequencydivider, mpegtype/IMpegAudioDecoder::put_FrequencyDivider, put_FrequencyDivider, put_FrequencyDivider method [DirectShow], put_FrequencyDivider method [DirectShow],IMpegAudioDecoder interface
f1_keywords:
- mpegtype/IMpegAudioDecoder.put_FrequencyDivider
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
- IMpegAudioDecoder.put_FrequencyDivider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMpegAudioDecoder::put_FrequencyDivider


## -description



Specifies the frequency divider as a three-level setting corresponding to the quality of CD Audio, FM Radio, or AM Radio.




## -parameters




### -param Divider [in]

Specifies the divider. 1 = "CD Audio"; 2 = "FM Radio"; 4 = "AM Radio".


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
 

 

