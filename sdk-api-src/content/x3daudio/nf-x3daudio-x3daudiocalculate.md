---
UID: NF:x3daudio.X3DAudioCalculate
title: X3DAudioCalculate function (x3daudio.h)
description: Calculates DSP settings with respect to 3D parameters.
helpviewer_keywords: ["X3DAudioCalculate","X3DAudioCalculate function [XAudio2 Audio Mixing APIs]","x3daudio/X3DAudioCalculate","xaudio2.x3daudiocalculate"]
old-location: xaudio2\x3daudiocalculate.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.x3daudio.X3DAudioCalculate(const X3DAUDIO_HANDLE,const X3DAUDIO_LISTENER,const X3DAUDIO_EMITTER,UINT32,X3DAUDIO_DSP_SETTINGS@)
ms.date: 12/05/2018
ms.keywords: X3DAudioCalculate, X3DAudioCalculate function [XAudio2 Audio Mixing APIs], x3daudio/X3DAudioCalculate, xaudio2.x3daudiocalculate
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
req.lib: Xaudio2.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X3DAudioCalculate
 - x3daudio/X3DAudioCalculate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - xaudio2.lib
 - xaudio2.dll
 - xaudio2_8.dll
 - xaudio2_9.dll
api_name:
 - X3DAudioCalculate
---

# X3DAudioCalculate function


## -description

Calculates DSP settings with respect to 3D parameters.

## -parameters

### -param Instance [in]

3D audio instance handle. Call <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize">X3DAudioInitialize</a> to get this handle.

### -param pListener [in]

Pointer to an <a href="/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener">X3DAUDIO_LISTENER</a> representing the point of reception.

### -param pEmitter [in]

Pointer to an <a href="/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter">X3DAUDIO_EMITTER</a> representing the sound source.

### -param Flags [in]

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>X3DAUDIO_CALCULATE_MATRIX</td>
<td>Enables matrix coefficient table calculation. </td>
</tr>
<tr>
<td>X3DAUDIO_CALCULATE_DELAY</td>
<td>Enables delay time array calculation (stereo only). </td>
</tr>
<tr>
<td>X3DAUDIO_CALCULATE_LPF_DIRECT</td>
<td>Enables low pass filter (LPF) direct-path coefficient calculation. </td>
</tr>
<tr>
<td>X3DAUDIO_CALCULATE_LPF_REVERB</td>
<td>Enables LPF reverb-path coefficient calculation. </td>
</tr>
<tr>
<td>X3DAUDIO_CALCULATE_REVERB</td>
<td>Enables reverb send level calculation. </td>
</tr>
<tr>
<td>X3DAUDIO_CALCULATE_DOPPLER</td>
<td>Enables Doppler shift factor calculation. </td>
</tr>
<tr>
<td>X3DAUDIO_CALCULATE_EMITTER_ANGLE</td>
<td>Enables emitter-to-listener interior angle calculation. </td>
</tr>
<tr>
<td>X3DAUDIO_CALCULATE_ZEROCENTER</td>
<td>Fills the center channel with silence.
         This flag allows you to keep a 6-channel matrix so you do not have to remap the channels, 
         but the center channel will be silent.  This flag is only valid if you also set
         X3DAUDIO_CALCULATE_MATRIX. </td>
</tr>
<tr>
<td>X3DAUDIO_CALCULATE_REDIRECT_TO_LFE</td>
<td>Applies an equal mix of all source channels
           to a low frequency effect (LFE) destination channel. It only applies to matrix calculations
           with a source that does not have an LFE channel and a destination that does have an LFE
           channel.  This flag is only valid  if you also set X3DAUDIO_CALCULATE_MATRIX. </td>
</tr>
</table>

### -param pDSPSettings [in, out]

Pointer to an <a href="/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings">X3DAUDIO_DSP_SETTINGS</a> structure that receives the calculation results.

## -returns

This function does not return a value.

## -remarks

You typically call <b>X3DAudioCalculate</b> once for each pair of emitting objects and listeners in the scene. After each call, to apply the 3D effects, the app manually applies the calculation results at <i>pDSPSettings</i> to the XAUDIO2 graph. For more info, see <a href="/windows/desktop/xaudio2/how-to--integrate-x3daudio-with-xaudio2">How to: Integrate X3DAudio with XAudio2</a>.

<div class="alert"><b>Important</b>   The listener and emitter values must be valid. Floating-point specials (NaN, QNaN, +INF, -INF) can cause the entire audio output to go silent if introduced into a running audio graph.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

<b>Windows Phone 8.1:</b> This API is supported.

## -see-also

<a href="/windows/desktop/xaudio2/functions">Functions</a>