---
UID: NS:xaudio2fx.XAUDIO2FX_REVERB_I3DL2_PARAMETERS
title: XAUDIO2FX_REVERB_I3DL2_PARAMETERS (xaudio2fx.h)
description: Describes I3DL2 (Interactive 3D Audio Rendering Guidelines Level 2.0) parameters for use in the ReverbConvertI3DL2ToNative function.
helpviewer_keywords: ["XAUDIO2FX_REVERB_I3DL2_PARAMETERS","XAUDIO2FX_REVERB_I3DL2_PARAMETERS structure [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2fx_reverb_i3dl2_parameters","xaudio2fx/XAUDIO2FX_REVERB_I3DL2_PARAMETERS"]
old-location: xaudio2\xaudio2fx_reverb_i3dl2_parameters.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2FX_REVERB_I3DL2_PARAMETERS
ms.date: 12/05/2018
ms.keywords: XAUDIO2FX_REVERB_I3DL2_PARAMETERS, XAUDIO2FX_REVERB_I3DL2_PARAMETERS structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2fx_reverb_i3dl2_parameters, xaudio2fx/XAUDIO2FX_REVERB_I3DL2_PARAMETERS
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
req.typenames: XAUDIO2FX_REVERB_I3DL2_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAUDIO2FX_REVERB_I3DL2_PARAMETERS
 - xaudio2fx/XAUDIO2FX_REVERB_I3DL2_PARAMETERS
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
 - XAUDIO2FX_REVERB_I3DL2_PARAMETERS
---

# XAUDIO2FX_REVERB_I3DL2_PARAMETERS structure


## -description

Describes I3DL2 (Interactive 3D Audio Rendering Guidelines Level 2.0) parameters for use in the <a href="/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative">ReverbConvertI3DL2ToNative</a> function.

## -struct-fields

### -field WetDryMix

Percentage of the output that will be reverb. Allowable values are from 0 to 100.

### -field Room

Attenuation of the room effect. Allowable values in hundredths of a decibel are from -10000 to 0.

### -field RoomHF

Attenuation of the room high-frequency effect. Allowable values in hundredths of a decibel are from -10000 to 0.

### -field RoomRolloffFactor

Rolloff factor for the reflected signals. Allowable values are from 0.0 to 10.0. Rolloff factor is ignored for built-in reverb effects.

### -field DecayTime

Reverberation decay time at low frequencies. Allowable values in seconds are from 0.1 to 20.0.

### -field DecayHFRatio

Ratio of the decay time at high frequencies to the decay time at low frequencies. Allowable values are from 0.1 to 2.0.

### -field Reflections

Attenuation of early reflections relative to <b>Room</b>. Allowable values in hundredths of a decibel are from -10000 to 1000.

### -field ReflectionsDelay

Delay time of the first reflection relative to the direct path. Allowable values in seconds are from 0.0 to 0.3.

### -field Reverb

Attenuation of late reverberation relative to <b>Room</b>. Allowable values in hundredths of a decibel are from -10000 to 2000.

### -field ReverbDelay

Time limit between the early reflections and the late reverberation relative to the time of the first reflection. Allowable values in seconds are from 0.0 to 0.1.

### -field Diffusion

Echo density in the late reverberation decay. Allowable values as a percentage are from 0 to 100.

### -field Density

Modal density in the late reverberation decay. Allowable values as a percentage are from 0 to 100.

### -field HFReference

Reference high frequency. Allowable values in Hz are from 20.0 to 20000.0.

## -remarks

There are many preset values defined for the <b>XAUDIO2FX_REVERB_I3DL2_PARAMETERS</b> structure. For more information, see <a href="/windows/desktop/xaudio2/xaudio2fx-i3dl2-preset">XAUDIO2FX_I3DL2_PRESET</a>.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative">ReverbConvertI3DL2ToNative</a>



<a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>



<a href="/windows/desktop/xaudio2/xaudio2fx-i3dl2-preset">XAUDIO2FX_I3DL2_PRESET</a>



<a href="/windows/desktop/xaudio2/structures">XAudio Structures</a>