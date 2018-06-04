---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IBDA_Encoder::EnumAudioCapability


## -description


Gets one of the audio formats supported by the device.


## -parameters




### -param FmtIndex [in]

The zero-based index of the audio format to retrieve. To get the number of audio formats, call <a href="https://msdn.microsoft.com/038f9360-0515-4655-9397-cd1bfb6c3d21">IBDA_Encoder::QueryCapabilities</a>. 


### -param MethodID [out]

Receives a value that uniquely identifies this audio method.


### -param AlgorithmType [out]

Receives the type of encoding algorithm. The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PBDA_Encoder_Audio_AlgorithmType_MPEG1LayerII"></a><a id="pbda_encoder_audio_algorithmtype_mpeg1layerii"></a><a id="PBDA_ENCODER_AUDIO_ALGORITHMTYPE_MPEG1LAYERII"></a><dl>
<dt><b>PBDA_Encoder_Audio_AlgorithmType_MPEG1LayerII</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
MPEG-1 Layer II.

</td>
</tr>
<tr>
<td width="40%"><a id="PBDA_Encoder_Audio_AlgorithmType_AC3"></a><a id="pbda_encoder_audio_algorithmtype_ac3"></a><a id="PBDA_ENCODER_AUDIO_ALGORITHMTYPE_AC3"></a><dl>
<dt><b>PBDA_Encoder_Audio_AlgorithmType_AC3</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Dolby AC3.

</td>
</tr>
</table>
 


### -param SamplingRate [out]

Receives the audio sampling rate, in Hz.


### -param BitDepth [out]

Receives the number of bits per audio sample.


### -param NumChannels [out]

Receives the number of audio channels.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/43ed9d91-c769-4fb3-bcd9-e5239ec5d9c7">IBDA_Encoder</a>
 

 

