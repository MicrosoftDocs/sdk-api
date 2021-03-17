---
UID: NS:x3daudio.X3DAUDIO_DSP_SETTINGS
title: X3DAUDIO_DSP_SETTINGS (x3daudio.h)
description: Receives the results from a call to X3DAudioCalculate.
helpviewer_keywords: ["*LPX3DAUDIO_DSP_SETTINGS","LPX3DAUDIO_DSP_SETTINGS","LPX3DAUDIO_DSP_SETTINGS structure pointer [XAudio2 Audio Mixing APIs]","X3DAUDIO_DSP_SETTINGS","X3DAUDIO_DSP_SETTINGS structure [XAudio2 Audio Mixing APIs]","x3daudio/LPX3DAUDIO_DSP_SETTINGS","x3daudio/X3DAUDIO_DSP_SETTINGS","xaudio2.x3daudio_dsp_settings"]
old-location: xaudio2\x3daudio_dsp_settings.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.x3daudio.X3DAUDIO_DSP_SETTINGS
ms.date: 12/05/2018
ms.keywords: '*LPX3DAUDIO_DSP_SETTINGS, LPX3DAUDIO_DSP_SETTINGS, LPX3DAUDIO_DSP_SETTINGS structure pointer [XAudio2 Audio Mixing APIs], X3DAUDIO_DSP_SETTINGS, X3DAUDIO_DSP_SETTINGS structure [XAudio2 Audio Mixing APIs], x3daudio/LPX3DAUDIO_DSP_SETTINGS, x3daudio/X3DAUDIO_DSP_SETTINGS, xaudio2.x3daudio_dsp_settings'
req.header: x3daudio.h
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
req.typenames: X3DAUDIO_DSP_SETTINGS, *LPX3DAUDIO_DSP_SETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X3DAUDIO_DSP_SETTINGS
 - x3daudio/X3DAUDIO_DSP_SETTINGS
 - LPX3DAUDIO_DSP_SETTINGS
 - x3daudio/LPX3DAUDIO_DSP_SETTINGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - x3daudio.h
api_name:
 - X3DAUDIO_DSP_SETTINGS
---

# X3DAUDIO_DSP_SETTINGS structure


## -description

Receives the results from a call to <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate">X3DAudioCalculate</a>.

## -struct-fields

### -field pMatrixCoefficients

Caller provided array that will be initialized with the volume level of each source channel present in each destination channel. The array must have at least (<b>SrcChannelCount</b> × <b>DstChannelCount</b>) elements. 
The array is arranged with the source channels as the column index of the array and the destination channels as the row index of the array. For example, when rendering two-channel stereo input into 5.1 output that is weighted toward the front channels—but is absent from the center and low-frequency channels—the matrix might be as shown in the following table.
      

<table>
<tr>
<th>Output</th>
<th>Left Input</th>
<th>Right Input</th>
</tr>
<tr>
<td>Left</td>
<td>1.0</td>
<td>0.0</td>
</tr>
<tr>
<td>Right</td>
<td>0.0</td>
<td>1.0</td>
</tr>
<tr>
<td>Front Center</td>
<td>0.0</td>
<td>0.0</td>
</tr>
<tr>
<td>LFE</td>
<td>0.0</td>
<td>0.0</td>
</tr>
<tr>
<td>Rear Left</td>
<td>0.8</td>
<td>0.0</td>
</tr>
<tr>
<td>Rear Right</td>
<td>0.0</td>
<td>0.8</td>
</tr>
</table>
 

Note that the left and right channels are fully mapped to the output left and right channels; 80 percent of the left and right input is mapped to the rear left and right channels.



The <b>pMatrixCoefficients</b> member can be NULL if the X3DAUDIO_CALCULATE_MATRIX flag is not specified when calling <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate">X3DAudioCalculate</a>.



When using X3DAudio with XAudio2 the value returned in the <b>pMatrixCoefficients</b> member would be applied to a voice with <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix">IXAudio2Voice::SetOutputMatrix</a>.

### -field pDelayTimes

Caller provided delay time array, which receives delays for each destination channel in milliseconds. This array must have at least <b>DstChannelCount</b> elements. X3DAudio doesn't actually perform the delay. It simply returns the coefficients that may be used to adjust a delay DSP effect placed in the effect chain. 
The <b>pDelayTimes</b> member can be NULL if the X3DAUDIO_CALCULATE_DELAY flag is not specified when calling <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate">X3DAudioCalculate</a>.


<div class="alert"><b>Note</b>  This member is only returned when X3DAudio is initialized for stereo output. For typical Xbox 360 usage, it will not return any data at all.</div>
<div> </div>

### -field SrcChannelCount

Number of source channels. This must be initialized to the number of emitter channels before calling <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate">X3DAudioCalculate</a>.

### -field DstChannelCount

Number of source channels. This must be initialized to the number of emitter channels before calling <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate">X3DAudioCalculate</a>.

### -field LPFDirectCoefficient

LPF direct-path coefficient. 
Only calculated if the X3DAUDIO_CALCULATE_LPF_DIRECT flag is specified when calling <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate">X3DAudioCalculate</a>.



When using X3DAudio with XAudio2 the value returned in the LPFDirectCoefficient member would be applied to a low pass filter on a source voice with <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters">IXAudio2Voice::SetFilterParameters</a>.

### -field LPFReverbCoefficient

LPF reverb-path coefficient. 


Only calculated if the X3DAUDIO_CALCULATE_LPF_REVERB flag is specified when calling <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate">X3DAudioCalculate</a>.

### -field ReverbLevel

Reverb send level. 
Only calculated if the X3DAUDIO_CALCULATE_REVERB flag is specified when calling <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate">X3DAudioCalculate</a>.

### -field DopplerFactor

Doppler shift factor. Scales the resampler ratio for Doppler shift effect, where: 



```
effective_frequency = DopplerFactor × original_frequency
```


Only calculated if the X3DAUDIO_CALCULATE_DOPPLER flag is specified when calling <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate">X3DAudioCalculate</a>.



When using X3DAudio with XAudio2 the value returned in the DopplerFactor would be applied to a source voice with <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio">IXAudio2SourceVoice::SetFrequencyRatio</a>.

### -field EmitterToListenerAngle

Emitter-to-listener interior angle, expressed in radians with respect to the emitter's front orientation. 


Only calculated if the X3DAUDIO_CALCULATE_EMITTER_ANGLE flag is specified when calling <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate">X3DAudioCalculate</a>.

### -field EmitterToListenerDistance

Distance in user-defined world units from the listener to the emitter base position.

### -field EmitterVelocityComponent

Component of emitter velocity vector projected onto emitter-to-listener vector in user-defined world units per second. 


Only calculated if the X3DAUDIO_CALCULATE_DOPPLER flag is specified when calling <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate">X3DAudioCalculate</a>.

### -field ListenerVelocityComponent

Component of listener velocity vector projected onto the emitter-&gt;listener vector in user-defined world units per second. 
Only calculated if the X3DAUDIO_CALCULATE_DOPPLER flag is specified when calling <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate">X3DAudioCalculate</a>.

## -remarks

The following members must be initialized before passing this structure to the <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate">X3DAudioCalculate</a> function:



<ul>
<li><b>pMatrixCoefficients

</b></li>
<li><b>pDelayTimes</b></li>
<li><b>SrcChannelCount

</b></li>
<li><b>DstChannelCount</b></li>
</ul>
The following members are returned by passing this structure to the <b>X3DAudioCalculate</b> function:

<ul>
<li><b>pMatrixCoefficients

</b></li>
<li><b>pDelayTimes

</b></li>
<li><b>LPFDirectCoefficient

</b></li>
<li><b>LPFReverbCoefficient</b></li>
<li><b>ReverbLevel

</b></li>
<li><b>DopplerFactor

</b></li>
<li><b>EmitterToListenerAngle</b></li>
<li><b>EmitterToListenerDistance

</b></li>
<li><b>EmitterVelocityComponent

</b></li>
<li><b>ListenerVelocityComponent</b></li>
</ul>
<div class="alert"><b>Note</b>  For <b>pMatrixCoefficients</b> and <b>pDelayTimes</b>, <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate">X3DAudioCalculate</a> does not allocate additional memory. <b>X3DAudioCalculate</b> merely modifies the values at the memory locations allocated for these pointers.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>