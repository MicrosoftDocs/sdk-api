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

# tagAecQualityMetrics_Struct structure


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
 

 

