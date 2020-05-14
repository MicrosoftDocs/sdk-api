---
UID: NF:mpegtype.IMpegAudioDecoder.get_DualMode
title: IMpegAudioDecoder::get_DualMode (mpegtype.h)
description: Returns which channel is currently being decoded.helpviewer_keywords: ["IMpegAudioDecoder interface [DirectShow]","get_DualMode method","IMpegAudioDecoder.get_DualMode","IMpegAudioDecoder::get_DualMode","IMpegAudioDecodergetDualMode","dshow.impegaudiodecoder_get_dualmode","get_DualMode","get_DualMode method [DirectShow]","get_DualMode method [DirectShow]","IMpegAudioDecoder interface","mpegtype/IMpegAudioDecoder::get_DualMode"]
old-location: dshow\impegaudiodecoder_get_dualmode.htm
tech.root: DirectShow
ms.assetid: 3b536e8c-91eb-4c32-955f-b343f2c8e16f
ms.date: 12/05/2018
ms.keywords: IMpegAudioDecoder interface [DirectShow],get_DualMode method, IMpegAudioDecoder.get_DualMode, IMpegAudioDecoder::get_DualMode, IMpegAudioDecodergetDualMode, dshow.impegaudiodecoder_get_dualmode, get_DualMode, get_DualMode method [DirectShow], get_DualMode method [DirectShow],IMpegAudioDecoder interface, mpegtype/IMpegAudioDecoder::get_DualMode
f1_keywords:
- mpegtype/IMpegAudioDecoder.get_DualMode
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
- IMpegAudioDecoder.get_DualMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMpegAudioDecoder::get_DualMode


## -description



Returns which channel is currently being decoded.




## -parameters




### -param pIntDecode [out]

Indicates the channel(s) to be decoded.


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
 




## -remarks



The <i>pIntDecode</i> parameter can have one of the values in the following table.

<table>
<tr>
<th>Constant
            </th>
<th>Description
            </th>
</tr>
<tr>
<td><b>AM_MPEG_AUDIO_DUAL_MERGE
            </b></td>
<td>Both channels are decoded.</td>
</tr>
<tr>
<td><b>AM_MPEG_AUDIO_DUAL_LEFT
            </b></td>
<td>The left channel is decoded.</td>
</tr>
<tr>
<td><b>AM_MPEG_AUDIO_DUAL_RIGHT
            </b></td>
<td>The right channel is decoded.</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mpegtype/nn-mpegtype-impegaudiodecoder">IMpegAudioDecoder</a>
 

 

