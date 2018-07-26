---
UID: NF:x3daudio.X3DAudioCalculate
title: X3DAudioCalculate function
author: windows-sdk-content
description: Calculates DSP settings with respect to 3D parameters.
old-location: xaudio2\x3daudiocalculate.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.x3daudio.X3DAudioCalculate(const X3DAUDIO_HANDLE,const X3DAUDIO_LISTENER,const X3DAUDIO_EMITTER,UINT32,X3DAUDIO_DSP_SETTINGS@)
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: X3DAudioCalculate, X3DAudioCalculate function [XAudio2 Audio Mixing APIs], x3daudio/X3DAudioCalculate, xaudio2.x3daudiocalculate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: ServerSelection
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - xaudio2.lib
 - xaudio2.dll
api_name:
 - X3DAudioCalculate
product: Windows
targetos: Windows
req.lib: Xaudio2.lib
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# X3DAudioCalculate function


## -description


Calculates DSP settings with respect to 3D parameters.


## -parameters




### -param Instance [in]

3D audio instance handle. Call <a href="https://msdn.microsoft.com/20f3d374-60bd-4a8c-8bd2-32e3be729779">X3DAudioInitialize</a> to get this handle.


### -param pListener [in]

Pointer to an <a href="https://msdn.microsoft.com/595578f8-9e1c-4905-b8a0-69182aac65b2">X3DAUDIO_LISTENER</a> representing the point of reception.


### -param pEmitter [in]

Pointer to an <a href="https://msdn.microsoft.com/13e6b0ae-79de-470e-93e2-fd3b96acd3ab">X3DAUDIO_EMITTER</a> representing the sound source.


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

Pointer to an <a href="https://msdn.microsoft.com/aed6351c-d34c-483b-b60d-875ef5fe11b4">X3DAUDIO_DSP_SETTINGS</a> structure that receives the calculation results.


## -returns



This function does not return a value.




## -remarks



You typically call <b>X3DAudioCalculate</b> once for each pair of emitting objects and listeners in the scene. After each call, to apply the 3D effects, the app manually applies the calculation results at <i>pDSPSettings</i> to the XAUDIO2 graph. For more info, see <a href="https://msdn.microsoft.com/a8f41f0d-b284-aefa-923b-471b13b4a3ec">How to: Integrate X3DAudio with XAudio2</a>.

<div class="alert"><b>Important</b>   The listener and emitter values must be valid. Floating-point specials (NaN, QNaN, +INF, -INF) can cause the entire audio output to go silent if introduced into a running audio graph.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

<b>Windows Phone 8.1:</b> This API is supported.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

