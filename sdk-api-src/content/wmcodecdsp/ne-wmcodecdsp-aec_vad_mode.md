---
UID: NE:wmcodecdsp.AEC_VAD_MODE
title: AEC_VAD_MODE (wmcodecdsp.h)
description: Specifies the type of voice activity detection (VAD) for the voice capture DSP. This enumeration is used with the MFPKEY_WMAAECMA_FEATR_VAD property.
helpviewer_keywords: ["AEC_VAD_DISABLED","AEC_VAD_FOR_AGC","AEC_VAD_FOR_SILENCE_SUPPRESSION","AEC_VAD_MODE","AEC_VAD_MODE enumeration [Media Foundation]","AEC_VAD_NORMAL","codecapi.aec_vad_modeenumeration","mf.aec_vad_modeenumeration","wmcodecdsp/AEC_VAD_DISABLED","wmcodecdsp/AEC_VAD_FOR_AGC","wmcodecdsp/AEC_VAD_FOR_SILENCE_SUPPRESSION","wmcodecdsp/AEC_VAD_MODE","wmcodecdsp/AEC_VAD_NORMAL"]
old-location: mf\aec_vad_modeenumeration.htm
tech.root: mf
ms.assetid: 01e2ba9e-1396-471e-a2bf-38dfcc7cac32
ms.date: 12/05/2018
ms.keywords: AEC_VAD_DISABLED, AEC_VAD_FOR_AGC, AEC_VAD_FOR_SILENCE_SUPPRESSION, AEC_VAD_MODE, AEC_VAD_MODE enumeration [Media Foundation], AEC_VAD_NORMAL, codecapi.aec_vad_modeenumeration, mf.aec_vad_modeenumeration, wmcodecdsp/AEC_VAD_DISABLED, wmcodecdsp/AEC_VAD_FOR_AGC, wmcodecdsp/AEC_VAD_FOR_SILENCE_SUPPRESSION, wmcodecdsp/AEC_VAD_MODE, wmcodecdsp/AEC_VAD_NORMAL
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AEC_VAD_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AEC_VAD_MODE
 - wmcodecdsp/AEC_VAD_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmcodecdsp.h
api_name:
 - AEC_VAD_MODE
---

# AEC_VAD_MODE enumeration


## -description

Specifies the type of voice activity detection (VAD) for the voice capture DSP. This enumeration is used with the <a href="/windows/desktop/medfound/mfpkey-wmaaecma-featr-vadproperty">MFPKEY_WMAAECMA_FEATR_VAD</a> property.

## -enum-fields

### -field AEC_VAD_DISABLED:0

Voice activity detection is disabled.

### -field AEC_VAD_NORMAL

General purpose VAD. This setting attempts to balance the false detection rate and the missed detection rate. The output can have the following values.
	     

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0</td>
<td>Non-speech.</td>
</tr>
<tr>
<td>1</td>
<td>Voiced speech.</td>
</tr>
<tr>
<td>2</td>
<td>Unvoiced speech.</td>
</tr>
<tr>
<td>3</td>
<td>Mixture of voiced and unvoiced speech.</td>
</tr>
</table>

### -field AEC_VAD_FOR_AGC

Voice activity detection for automatic gain control and noise suppression. In this mode, the VAD threshold is higher than the normal mode, to reduce the false detection rate. The output distinguishes voiced speech from other sounds (non-speech or unvoiced speech). The output can have the following values.
        

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0</td>
<td>Non-speech or unvoiced speech.</td>
</tr>
<tr>
<td>1</td>
<td>Voiced speech.</td>
</tr>
</table>

### -field AEC_VAD_FOR_SILENCE_SUPPRESSION

Voice activity detection for silence suppression. In this mode, the output distinguishes speech (voiced or unvoiced) from non-speech. The output can have the following values.
        

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0</td>
<td>Non-speech.</td>
</tr>
<tr>
<td>1</td>
<td>Voiced or unvoiced speech.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/voicecapturedmo">Voice Capture</a>
