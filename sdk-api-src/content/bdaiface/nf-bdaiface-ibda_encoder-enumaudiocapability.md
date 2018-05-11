---
UID: NF:bdaiface.IBDA_Encoder.EnumAudioCapability
title: IBDA_Encoder::EnumAudioCapability
author: windows-driver-content
description: Gets one of the audio formats supported by the device.
old-location: mstv\ibda_encoder_enumaudiocapability.htm
old-project: mstv
ms.assetid: 5dcc8f5e-c8bc-4443-bb07-0eb48bb72738
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: EnumAudioCapability, EnumAudioCapability method [Microsoft TV Technologies], EnumAudioCapability method [Microsoft TV Technologies],IBDA_Encoder interface, IBDA_Encoder interface [Microsoft TV Technologies],EnumAudioCapability method, IBDA_Encoder.EnumAudioCapability, IBDA_Encoder::EnumAudioCapability, PBDA_Encoder_Audio_AlgorithmType_AC3, PBDA_Encoder_Audio_AlgorithmType_MPEG1LayerII, bdaiface/IBDA_Encoder::EnumAudioCapability, mstv.ibda_encoder_enumaudiocapability
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_Encoder.EnumAudioCapability
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

