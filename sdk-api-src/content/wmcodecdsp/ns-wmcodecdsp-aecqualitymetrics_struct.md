---
UID: NS:wmcodecdsp.tagAecQualityMetrics_Struct
title: AecQualityMetrics_Struct (wmcodecdsp.h)
description: Contains quality metrics for acoustic echo cancellation (AEC). This structure is used with the MFPKEY_WMAAECMA_RETRIEVE_TS_STATS property.
helpviewer_keywords: ["AecQualityMetrics_Struct","AecQualityMetrics_Struct structure [Media Foundation]","codecapi.aecqualitymetrics_structstructure","codecapi.mic_array_modeenumeration","mf.aecqualitymetrics_structstructure","wmcodecdsp/AecQualityMetrics_Struct"]
old-location: mf\aecqualitymetrics_structstructure.htm
tech.root: mf
ms.assetid: 1a44d12c-3da9-4fcb-a4ba-4a405882c134
ms.date: 12/05/2018
ms.keywords: AecQualityMetrics_Struct, AecQualityMetrics_Struct structure [Media Foundation], codecapi.aecqualitymetrics_structstructure, codecapi.mic_array_modeenumeration, mf.aecqualitymetrics_structstructure, wmcodecdsp/AecQualityMetrics_Struct
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
req.typenames: AecQualityMetrics_Struct
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAecQualityMetrics_Struct
 - wmcodecdsp/tagAecQualityMetrics_Struct
 - AecQualityMetrics_Struct
 - wmcodecdsp/AecQualityMetrics_Struct
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
 - AecQualityMetrics_Struct
---

# AecQualityMetrics_Struct structure


## -description

Contains quality metrics for acoustic echo cancellation (AEC). This structure is used with the <a href="/windows/desktop/medfound/mfpkey-wmaaecma-retrieve-ts-statsproperty">MFPKEY_WMAAECMA_RETRIEVE_TS_STATS</a> property.

## -struct-fields

### -field i64Timestamp

Time stamp that indicates when the quality metrics were collected.

### -field ConvergenceFlag

AEC convergence flag.

### -field MicClippedFlag

If <b>TRUE</b>, the input signal from the audio capture device was clipped.

### -field MicSilenceFlag

If <b>TRUE</b>, the input signal from the audio capture device was silent or too quiet.

### -field PstvFeadbackFlag

If <b>TRUE</b>, positive feedback is causing a chirping sound.

### -field SpkClippedFlag

If <b>TRUE</b>, the input signal from the audio rendering device was clipped.

### -field SpkMuteFlag

If <b>TRUE</b>, the input signal from the audio rendering device was silent or too quiet.

### -field GlitchFlag

A glitch occurred in the input data.

### -field DoubleTalkFlag

Double talk flag.

### -field uGlitchCount

Number of glitches.

### -field uMicClipCount

Number of times the audio capture signal was clipped.

### -field fDuration

Running duration of the AEC process.

### -field fTSVariance

Long-term average variance in the time stamps.

### -field fTSDriftRate

Long-term average drift rate in the time stamps.

### -field fVoiceLevel

Near-end voice level after AEC processing.

### -field fNoiseLevel

Noise level of the audio capture signal.

### -field fERLE

Echo return loss enhancement (ERLE).

### -field fAvgERLE

Average ERLE over the entire duration of AEC processing.

### -field dwReserved

Reserved

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/voicecapturedmo">Voice Capture DSP</a>