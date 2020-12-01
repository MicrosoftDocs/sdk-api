---
UID: NS:xaudio2fx.XAUDIO2FX_REVERB_PARAMETERS
title: XAUDIO2FX_REVERB_PARAMETERS (xaudio2fx.h)
description: Describes parameters for use in the reverb APO.
helpviewer_keywords: ["XAUDIO2FX_REVERB_PARAMETERS","XAUDIO2FX_REVERB_PARAMETERS structure [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2fx_reverb_parameters","xaudio2fx/XAUDIO2FX_REVERB_PARAMETERS"]
old-location: xaudio2\xaudio2fx_reverb_parameters.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2FX_REVERB_PARAMETERS
ms.date: 12/05/2018
ms.keywords: XAUDIO2FX_REVERB_PARAMETERS, XAUDIO2FX_REVERB_PARAMETERS structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2fx_reverb_parameters, xaudio2fx/XAUDIO2FX_REVERB_PARAMETERS
req.header: xaudio2fx.h
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
req.typenames: XAUDIO2FX_REVERB_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAUDIO2FX_REVERB_PARAMETERS
 - xaudio2fx/XAUDIO2FX_REVERB_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2fx.h
api_name:
 - XAUDIO2FX_REVERB_PARAMETERS
---

# XAUDIO2FX_REVERB_PARAMETERS structure


## -description

Describes parameters for use in the reverb APO.

## -struct-fields

### -field WetDryMix

Percentage of the output that will be reverb. Allowable values are from 0 to 100.

### -field ReflectionsDelay

The delay time of the first reflection relative to the direct path. Permitted range is from 0 to 300 milliseconds. 

<div class="alert"><b>Note</b>  All parameters related to sampling rate or time are relative to a 48kHz sampling rate and must be scaled for use with other sampling rates. See remarks section below for additional information.</div>
<div> </div>

### -field ReverbDelay

Delay of reverb relative to the first reflection. Permitted range is from 0 to 85 milliseconds.

<div class="alert"><b>Note</b>  All parameters related to sampling rate or time are relative to a 48kHz sampling rate and must be scaled for use with other sampling rates. See remarks section below for additional information.</div>
<div> </div>

### -field RearDelay

Delay for the left rear output and right rear output. Permitted range is from 0 to 5 milliseconds.

<div class="alert"><b>Note</b>  All parameters related to sampling rate or time are relative to a 48kHz sampling rate and must be scaled for use with other sampling rates. See remarks section below for additional information.</div>
<div> </div>

### -field SideDelay

Delay for the left side output and right side output. Permitted range is from 0 to 5 milliseconds.

<div class="alert"><b>Note</b>  This value is supported beginning with Windows 10.</div>
<div> </div>
<div class="alert"><b>Note</b>  All parameters related to sampling rate or time are relative to a 48kHz sampling rate and must be scaled for use with other sampling rates. See remarks section below for additional information.</div>
<div> </div>

### -field PositionLeft

Position of the left input within the simulated space relative to the listener. With <i>PositionLeft</i> set to the minimum value, the left input is placed close to the listener. In this position, early reflections are dominant, and the reverb decay is set back in the sound field and reduced in amplitude. With <i>PositionLeft</i> set to the maximum value, the left input is placed at a maximum distance from the listener within the simulated room. <i>PositionLeft</i> does not affect the reverb decay time (liveness of the room), only the apparent position of the source relative to the listener. Permitted range is from 0 to 30 (no units).

### -field PositionRight

Same as <i>PositionLeft</i>, but affecting only the right input. Permitted range is from 0 to 30 (no units). 

<div class="alert"><b>Note</b>  PositionRight is ignored in mono-in/mono-out mode.</div>
<div> </div>

### -field PositionMatrixLeft

Gives a greater or lesser impression of distance from the source to the listener. Permitted range is from 0 to 30 (no units).

### -field PositionMatrixRight

Gives a greater or lesser impression of distance from the source to the listener. Permitted range is from 0 to 30 (no units). 

<div class="alert"><b>Note</b>  <i>PositionMatrixRight</i> is ignored in mono-in/mono-out mode.</div>
<div> </div>

### -field EarlyDiffusion

Controls the character of the individual wall reflections. Set to minimum value to simulate a hard flat surface and to maximum value to simulate a diffuse surface. Permitted range is from 0 to 15 (no units).

### -field LateDiffusion

Controls the character of the individual wall reverberations. Set to minimum value to simulate a hard flat surface and to maximum value to simulate a diffuse surface. Permitted range is from 0 to 15 (no units).

### -field LowEQGain

Adjusts the decay time of low frequencies relative to the decay time at 1 kHz. The values correspond to dB of gain as follows: 
       

<table>
<tr>
<th>Value</th>
<td>0</td>
<td>1</td>
<td>2</td>
<td>3</td>
<td>4</td>
<td>5</td>
<td>6</td>
<td>7</td>
<td>8</td>
<td>9</td>
<td>10</td>
<td>11</td>
<td>12</td>
</tr>
<tr>
<th>Gain (dB)</th>
<td>-8</td>
<td>-7</td>
<td>-6</td>
<td>-5</td>
<td>-4</td>
<td>-3</td>
<td>-2</td>
<td>-1</td>
<td>0</td>
<td>+1</td>
<td>+2</td>
<td>+3</td>
<td>+4</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  A <i>LowEQGain</i> value of 8 results in the decay time of low frequencies being equal to the decay time at 1 kHz.</div>
<div> </div>
 Permitted range is from 0 to 12 (no units).

### -field LowEQCutoff

Sets the corner frequency of the low pass filter that is controlled by the <i>LowEQGain</i> parameter. The values correspond to frequency in Hz as follows: 
       

<table>
<tr>
<th>Value</th>
<td>0</td>
<td>1</td>
<td>2</td>
<td>3</td>
<td>4</td>
<td>5</td>
<td>6</td>
<td>7</td>
<td>8</td>
<td>9</td>
</tr>
<tr>
<th>Frequency (Hz)</th>
<td>50</td>
<td>100</td>
<td>150</td>
<td>200</td>
<td>250</td>
<td>300</td>
<td>350</td>
<td>400</td>
<td>450</td>
<td>500</td>
</tr>
</table>
 

Permitted range is from 0 to 9 (no units).

### -field HighEQGain

Adjusts the decay time of high frequencies relative to the decay time at 1 kHz. When set to zero, high frequencies decay at the same rate as 1 kHz. When set to maximum value, high frequencies decay at a much faster rate than 1 kHz.
	        

<table>
<tr>
<th>Value</th>
<td>0</td>
<td>1</td>
<td>2</td>
<td>3</td>
<td>4</td>
<td>5</td>
<td>6</td>
<td>7</td>
<td>8</td>
</tr>
<tr>
<th>Gain (dB)</th>
<td>-8</td>
<td>-7</td>
<td>-6</td>
<td>-5</td>
<td>-4</td>
<td>-3</td>
<td>-2</td>
<td>-1</td>
<td>0</td>
</tr>
</table>
 

Permitted range is from 0 to 8 (no units).

### -field HighEQCutoff

Sets the corner frequency of the high pass filter that is controlled by the <i>HighEQGain</i> parameter. The values correspond to frequency in kHz as follows:       

<table>
<tr>
<th>Value</th>
<td>0</td>
<td>1</td>
<td>2</td>
<td>3</td>
<td>4</td>
<td>5</td>
<td>6</td>
<td>7</td>
<td>8</td>
<td>9</td>
<td>10</td>
<td>11</td>
<td>12</td>
<td>13</td>
<td>14</td>
</tr>
<tr>
<th>Frequency (kHz)</th>
<td>1</td>
<td>1.5</td>
<td>2</td>
<td>2.5</td>
<td>3</td>
<td>3.5</td>
<td>4</td>
<td>4.5</td>
<td>5</td>
<td>5.5</td>
<td>6</td>
<td>6.5</td>
<td>7</td>
<td>7.5</td>
<td>8</td>
</tr>
</table>
 

Permitted range is from 0 to 14 (no units).

### -field RoomFilterFreq

Sets the corner frequency of the low pass filter for the room effect. Permitted range is from 20 to 20,000 Hz.

<div class="alert"><b>Note</b>  All parameters related to sampling rate or time are relative to a 48kHz sampling rate and must be scaled for use with other sampling rates. See remarks section below for additional information.</div>
<div> </div>

### -field RoomFilterMain

Sets the pass band intensity level of the low-pass filter for both the early reflections and the late field reverberation. Permitted range is from -100 to 0 dB.

### -field RoomFilterHF

Sets the intensity of the low-pass filter for both the early reflections and the late field reverberation at the corner frequency (<i>RoomFilterFreq</i>). Permitted range is from -100 to 0 dB.

### -field ReflectionsGain

Adjusts the intensity of the early reflections. Permitted range is from -100 to 20 dB.

### -field ReverbGain

Adjusts the intensity of the reverberations. Permitted range is from -100 to 20 dB.

### -field DecayTime

Reverberation decay time at 1 kHz. This is the time that a full scale input signal decays by 60 dB. Permitted range is from 0.1 to infinity seconds.

### -field Density

Controls the modal density in the late field reverberation. For colorless spaces, <i>Density</i> should be set to the maximum value (100). As Density is decreased, the sound becomes hollow (comb filtered). This is an effect that can be useful if you are trying to model a silo. Permitted range as a percentage is from 0 to 100.

### -field RoomSize

The apparent size of the acoustic space. Permitted range is from 1 to 100 feet.

### -field DisableLateField

If set to TRUE, disables late field reflection calculations. Disabling late field reflection calculations results in a significant CPU time savings.

<div class="alert"><b>Note</b>  The DirectX SDK versions of XAUDIO2 don't support this member.</div>
<div> </div>

## -remarks

All parameters related to sampling rate or time are relative to a 48kHz voice and must be scaled for use with other sampling rates. For example, setting <i>ReflectionsDelay</i> to 300ms gives a true 300ms delay when the reverb is hosted in a 48kHz voice, but becomes a 150ms delay when hosted in a 24kHz voice.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--create-an-effect-chain">How to: Create an Effect Chain</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters">IXAudio2Voice::SetEffectParameters</a>



<a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>



<a href="/windows/desktop/xaudio2/structures">XAudio Structures</a>



<a href="/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb">XAudio2CreateReverb</a>