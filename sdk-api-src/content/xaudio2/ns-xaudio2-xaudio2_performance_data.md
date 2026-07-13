---
UID: NS:xaudio2.XAUDIO2_PERFORMANCE_DATA
title: XAUDIO2_PERFORMANCE_DATA (xaudio2.h)
description: Contains performance information. (XAUDIO2_PERFORMANCE_DATA)
helpviewer_keywords: ["XAUDIO2_PERFORMANCE_DATA","XAUDIO2_PERFORMANCE_DATA structure [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2_performance_data","xaudio2/XAUDIO2_PERFORMANCE_DATA"]
old-location: xaudio2\xaudio2_performance_data.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_PERFORMANCE_DATA
ms.date: 12/05/2018
ms.keywords: XAUDIO2_PERFORMANCE_DATA, XAUDIO2_PERFORMANCE_DATA structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_performance_data, xaudio2/XAUDIO2_PERFORMANCE_DATA
req.header: xaudio2.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XAUDIO2_PERFORMANCE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAUDIO2_PERFORMANCE_DATA
 - xaudio2/XAUDIO2_PERFORMANCE_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAUDIO2_PERFORMANCE_DATA
---

# XAUDIO2_PERFORMANCE_DATA structure


## -description

Contains performance information.

## -struct-fields

### -field AudioCyclesSinceLastQuery

CPU cycles spent on audio processing since the last call to the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-startengine">IXAudio2::StartEngine</a> or <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata">IXAudio2::GetPerformanceData</a> function.

### -field TotalCyclesSinceLastQuery

Total CPU cycles elapsed since the last call. 

<div class="alert"><b>Note</b>  This only counts cycles on the CPU on which XAudio2 is running.</div>
<div> </div>

### -field MinimumCyclesPerQuantum

Fewest CPU cycles spent on processing any single audio quantum since the last call.

### -field MaximumCyclesPerQuantum

Most CPU cycles spent on processing any single audio quantum since the last call.

### -field MemoryUsageInBytes

Total memory currently in use.

### -field CurrentLatencyInSamples

Minimum delay that occurs between the time a sample is read from a source buffer and the time it reaches the speakers. 

<table>
<tr>
<th>Windows</th>
</tr>
<tr>
<td>The delay reported is a variable value equal to the rough distance between the last sample submitted to the driver by XAudio2 and the sample currently playing. The following factors can affect the delay: playing multichannel audio on a hardware-accelerated device; the type of audio device (WavePci, WaveCyclic, or WaveRT); and, to a lesser extent, audio hardware implementation.
</td>
</tr>
</table>
 

<table>
<tr>
<th>Xbox 360</th>
</tr>
<tr>
<td>The delay reported is a fixed value, which is normally 1,024 samples (21.333 ms at 48 kHz). If <b>XOverrideSpeakerConfig</b> has been called using the <b>XAUDIOSPEAKERCONFIG_LOW_LATENCY</b> flag, the delay reported is 512 samples (10.667 ms at 48 kHz).
</td>
</tr>
</table>

### -field GlitchesSinceEngineStarted

Total audio dropouts since the engine started.

### -field ActiveSourceVoiceCount

Number of source voices currently playing.

### -field TotalSourceVoiceCount

Total number of source voices currently in existence.

### -field ActiveSubmixVoiceCount

Number of submix voices currently playing.

### -field ActiveResamplerCount

Number of resampler xAPOs currently active.

### -field ActiveMatrixMixCount

Number of matrix mix xAPOs currently active.

### -field ActiveXmaSourceVoices

<table>
<tr>
<th>Windows</th>
</tr>
<tr>
<td>Unsupported.</td>
</tr>
</table>
 

<table>
<tr>
<th>Xbox 360</th>
</tr>
<tr>
<td>Number of source voices decoding XMA data.</td>
</tr>
</table>

### -field ActiveXmaStreams

<table>
<tr>
<th>Windows</th>
</tr>
<tr>
<td>Unsupported.</td>
</tr>
</table>
 

<table>
<tr>
<th>Xbox 360</th>
</tr>
<tr>
<td>A voice can use more than one XMA stream.</td>
</tr>
</table>

## -remarks

CPU cycles are recorded using . Use to convert these values.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata">IXAudio2::GetPerformanceData</a>



<a href="/windows/desktop/xaudio2/structures">XAudio2 Structures</a>
