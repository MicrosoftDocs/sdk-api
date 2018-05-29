---
UID: NF:mpegtype.IMpegAudioDecoder.put_DualMode
title: IMpegAudioDecoder::put_DualMode
author: windows-sdk-content
description: Specifies the channel to be decoded.
old-location: dshow\impegaudiodecoder_put_dualmode.htm
old-project: DirectShow
ms.assetid: b183f669-14bf-44d4-a17d-09cbc593309d
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IMpegAudioDecoder interface [DirectShow],put_DualMode method, IMpegAudioDecoder.put_DualMode, IMpegAudioDecoder::put_DualMode, IMpegAudioDecoderputDualMode, dshow.impegaudiodecoder_put_dualmode, mpegtype/IMpegAudioDecoder::put_DualMode, put_DualMode, put_DualMode method [DirectShow], put_DualMode method [DirectShow],IMpegAudioDecoder interface
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
-	IMpegAudioDecoder.put_DualMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMpegAudioDecoder::put_DualMode


## -description



Specifies the channel to be decoded.




## -parameters




### -param IntDecode [in]

Specifies the channel(s) to be decoded. See remarks for valid values.


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



The following table lists the valid values for the <i>pIntDecode</i> parameter.

<table>
<tr>
<th>
              Constant
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td><b>
              AM_MPEG_AUDIO_DUAL_MERGE
            </b></td>
<td>Specifies that both channels will be decoded.</td>
</tr>
<tr>
<td><b>
              AM_MPEG_AUDIO_DUAL_LEFT
            </b></td>
<td>Specifies that the left channel will be decoded.</td>
</tr>
<tr>
<td><b>
              AM_MPEG_AUDIO_DUAL_RIGHT
            </b></td>
<td>Specifies that the right channel will be decoded.</td>
</tr>
</table>
 

This method is useful for karaoke discs in Video CD (VCD) format that have two mono channels in the audio stream.




## -see-also




<a href="https://msdn.microsoft.com/59fd96ef-2f9a-4a8e-bd08-2695de52b1c6">IMpegAudioDecoder</a>
 

 

