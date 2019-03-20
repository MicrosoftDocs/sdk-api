---
UID: NS:wmcodecdsp.tagAecQualityMetrics_Struct
title: AecQualityMetrics_Struct (wmcodecdsp.h)
author: windows-sdk-content
description: Contains quality metrics for acoustic echo cancellation (AEC). This structure is used with the MFPKEY_WMAAECMA_RETRIEVE_TS_STATS property.
old-location: mf\aecqualitymetrics_structstructure.htm
tech.root: medfound
ms.assetid: 1a44d12c-3da9-4fcb-a4ba-4a405882c134
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AecQualityMetrics_Struct, AecQualityMetrics_Struct structure [Media Foundation], codecapi.aecqualitymetrics_structstructure, codecapi.mic_array_modeenumeration, mf.aecqualitymetrics_structstructure, wmcodecdsp/AecQualityMetrics_Struct
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmcodecdsp.h
api_name:
 - AecQualityMetrics_Struct
product: Windows
targetos: Windows
req.typenames: AecQualityMetrics_Struct
req.redist: 
---

# AecQualityMetrics_Struct structure


## -description


Contains quality metrics for acoustic echo cancellation (AEC). This structure is used with the <a href="https://msdn.microsoft.com/c44462be-ccdf-4a49-bb77-6e816def4849">MFPKEY_WMAAECMA_RETRIEVE_TS_STATS</a> property.



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




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/6c77c8f6-289e-4130-b56a-e1f0bcc40f3e">Voice Capture DSP</a>
 

 

