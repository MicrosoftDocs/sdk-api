---
UID: NF:bdaiface.IBDA_Encoder.EnumAudioCapability
title: IBDA_Encoder::EnumAudioCapability (bdaiface.h)
description: Gets one of the audio formats supported by the device.
helpviewer_keywords: ["EnumAudioCapability","EnumAudioCapability method [Microsoft TV Technologies]","EnumAudioCapability method [Microsoft TV Technologies]","IBDA_Encoder interface","IBDA_Encoder interface [Microsoft TV Technologies]","EnumAudioCapability method","IBDA_Encoder.EnumAudioCapability","IBDA_Encoder::EnumAudioCapability","PBDA_Encoder_Audio_AlgorithmType_AC3","PBDA_Encoder_Audio_AlgorithmType_MPEG1LayerII","bdaiface/IBDA_Encoder::EnumAudioCapability","mstv.ibda_encoder_enumaudiocapability"]
old-location: mstv\ibda_encoder_enumaudiocapability.htm
tech.root: mstv
ms.assetid: 5dcc8f5e-c8bc-4443-bb07-0eb48bb72738
ms.date: 12/05/2018
ms.keywords: EnumAudioCapability, EnumAudioCapability method [Microsoft TV Technologies], EnumAudioCapability method [Microsoft TV Technologies],IBDA_Encoder interface, IBDA_Encoder interface [Microsoft TV Technologies],EnumAudioCapability method, IBDA_Encoder.EnumAudioCapability, IBDA_Encoder::EnumAudioCapability, PBDA_Encoder_Audio_AlgorithmType_AC3, PBDA_Encoder_Audio_AlgorithmType_MPEG1LayerII, bdaiface/IBDA_Encoder::EnumAudioCapability, mstv.ibda_encoder_enumaudiocapability
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_Encoder::EnumAudioCapability
 - bdaiface/IBDA_Encoder::EnumAudioCapability
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_Encoder.EnumAudioCapability
---

# IBDA_Encoder::EnumAudioCapability


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets one of the audio formats supported by the device.

## -parameters

### -param FmtIndex [in]

The zero-based index of the audio format to retrieve. To get the number of audio formats, call <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_encoder-querycapabilities">IBDA_Encoder::QueryCapabilities</a>.

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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_encoder">IBDA_Encoder</a>