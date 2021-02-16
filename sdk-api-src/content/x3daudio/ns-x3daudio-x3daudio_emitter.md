---
UID: NS:x3daudio.X3DAUDIO_EMITTER
title: X3DAUDIO_EMITTER (x3daudio.h)
description: Defines a single-point or multiple-point 3D audio source that is used with an arbitrary number of sound channels.
helpviewer_keywords: ["*LPX3DAUDIO_EMITTER","LPX3DAUDIO_EMITTER","LPX3DAUDIO_EMITTER structure pointer [XAudio2 Audio Mixing APIs]","X3DAUDIO_EMITTER","X3DAUDIO_EMITTER structure [XAudio2 Audio Mixing APIs]","x3daudio/LPX3DAUDIO_EMITTER","x3daudio/X3DAUDIO_EMITTER","xaudio2.x3daudio_emitter"]
old-location: xaudio2\x3daudio_emitter.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.x3daudio.X3DAUDIO_EMITTER
ms.date: 12/05/2018
ms.keywords: '*LPX3DAUDIO_EMITTER, LPX3DAUDIO_EMITTER, LPX3DAUDIO_EMITTER structure pointer [XAudio2 Audio Mixing APIs], X3DAUDIO_EMITTER, X3DAUDIO_EMITTER structure [XAudio2 Audio Mixing APIs], x3daudio/LPX3DAUDIO_EMITTER, x3daudio/X3DAUDIO_EMITTER, xaudio2.x3daudio_emitter'
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
req.typenames: X3DAUDIO_EMITTER, *LPX3DAUDIO_EMITTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X3DAUDIO_EMITTER
 - x3daudio/X3DAUDIO_EMITTER
 - LPX3DAUDIO_EMITTER
 - x3daudio/LPX3DAUDIO_EMITTER
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
 - X3DAUDIO_EMITTER
---

# X3DAUDIO_EMITTER structure


## -description

Defines a single-point or multiple-point 3D audio source that is used with an arbitrary number of sound channels.

## -struct-fields

### -field pCone

Pointer to a sound cone. Used only with single-channel emitters for matrix, LPF (both direct and reverb paths), and reverb calculations. NULL specifies the emitter is omnidirectional.

### -field OrientFront

Orientation of the front direction. This value must be orthonormal with <b>OrientTop</b>. <b>OrientFront</b> must be normalized when used. For single-channel emitters without cones <b>OrientFront</b> is only used for emitter angle calculations. For multi channel emitters or single-channel with cones <b>OrientFront</b> is used for matrix, LPF (both direct and reverb paths), and reverb calculations.

### -field OrientTop

Orientation of the top direction. This value must be orthonormal with <b>OrientFront</b>. <b>OrientTop</b> is only used with multi-channel emitters for matrix calculations.

### -field Position

Position in user-defined world units. This value does not affect <b>Velocity</b>.

### -field Velocity

Velocity vector in user-defined world units/second. This value is used only for doppler calculations. It does not affect <b>Position</b>.

### -field InnerRadius

Value to be used for the inner radius calculations. If <b>InnerRadius</b> is 0, then no inner radius is used, but <b>InnerRadiusAngle</b> may still be used. This value must be between 0.0f and MAX_FLT.

### -field InnerRadiusAngle

Value to be used for the inner radius angle calculations. This value must be between 0.0f and X3DAUDIO_PI/4.0.

### -field ChannelCount

Number of emitters defined by the <b>X3DAUDIO_EMITTER</b> structure. Must be greater than 0.

### -field ChannelRadius

Distance from <b>Position</b> that channels will be placed if <b>ChannelCount</b> is greater than 1. <b>ChannelRadius</b> is only used with multi-channel emitters for matrix calculations. Must be greater than or equal to 0.0f.

### -field pChannelAzimuths

Table of channel positions, expressed as an azimuth in radians along the channel radius with respect to the front orientation vector in the plane orthogonal to the top orientation vector. An azimuth of X3DAUDIO_2PI specifies a channel is a low-frequency effects (LFE) channel. LFE channels are positioned at the emitter base and are calculated with respect to <b>pLFECurve</b> only, never <b>pVolumeCurve</b>. <b>pChannelAzimuths</b> must have at least <b>ChannelCount</b> elements, but can be <b>NULL</b> if <b>ChannelCount</b> = 1. The table values must be within 0.0f to X3DAUDIO_2PI. <b>pChannelAzimuths</b> is used with multi-channel emitters for matrix calculations.

### -field pVolumeCurve

Volume-level distance curve, which is used only for matrix calculations. NULL specifies a specialized default curve that conforms to the inverse square law, such that when distance is between 0.0f and <b>CurveDistanceScaler</b> × 1.0f, no attenuation is applied. 
When distance is greater than <b>CurveDistanceScaler</b> × 1.0f, the amplification factor is (<b>CurveDistanceScaler</b> × 1.0f)/distance. At a distance of <b>CurveDistanceScaler</b> × 2.0f, the sound will be at half volume or -6 dB, at a distance of <b>CurveDistanceScaler</b> × 4.0f, the sound will be at one quarter volume or -12 dB, and so on.

<b>pVolumeCurve</b> and pLFECurve are independent of each other. <b>pVolumeCurve</b> does not affect <b>LFE channel</b> volume.

### -field pLFECurve

LFE roll-off distance curve, or NULL to use default curve: [0.0f, <b>CurveDistanceScaler</b> ×1.0f], [<b>CurveDistanceScaler</b> ×1.0f, 0.0f]. A NULL value for <b>pLFECurve</b> specifies a default curve that conforms to the inverse square law with distances &lt;= <b>CurveDistanceScaler</b> clamped to no attenuation. 
<b>pVolumeCurve</b> and <b>pLFECurve</b> are independent of each other. <b>pLFECurve</b> does not affect non LFE channel volume.

### -field pLPFDirectCurve

Low-pass filter (LPF) direct-path coefficient distance curve, or NULL to use the default curve: [0.0f, 1.0f], [1.0f, 0.75f]. <b>pLPFDirectCurve</b> is only used for LPF direct-path calculations.

### -field pLPFReverbCurve

LPF reverb-path coefficient distance curve, or NULL to use default curve: [0.0f, 0.75f], [1.0f, 0.75f]. <b>pLPFReverbCurve</b> is only used for LPF reverb path calculations.

### -field pReverbCurve

Reverb send level distance curve, or NULL to use default curve: [0.0f, 1.0f], [1.0f, 0.0f].

### -field CurveDistanceScaler

Curve distance scaler that is used to scale normalized distance curves to user-defined world units, and/or to exaggerate their effect. This does not affect any other calculations. The value must be within the range FLT_MIN to FLT_MAX. <b>CurveDistanceScaler</b> is only used for matrix, LPF (both direct and reverb paths), and reverb calculations.

### -field DopplerScaler

Doppler shift scaler that is used to exaggerate Doppler shift effect. <b>DopplerScaler</b> is only used for Doppler calculations and does not affect any other calculations. The value must be within the range 0.0f to FLT_MAX.

## -remarks

<b>X3DAUDIO_EMITTER</b> only supports a cone in a single-point emitter. Multi-point emitters are a convenient and efficient way to manage a related group of sound sources. Many properties are shared among all channel points, such as Doppler—the same Doppler shift is applied to all channels in the emitter. Thus, the Doppler value need only be calculated once, not per-point as would be needed with multiple separate single-point emitters. Because <b>X3DAUDIO_EMITTER</b> only has one orientation vector, a multi-point emitter cone would be of limited usefulness, forcing all channels to behave as if they were facing the same direction. If multiple independent cones are needed, multiple single-point emitters should be used, each with its own orientation.



The parameter type X3DAUDIO_VECTOR is typed to DirectX::XMFLOAT3, to provide x , y , and z floating-point values.



X3DAudio uses a left-handed Cartesian coordinate system, with values on the x-axis increasing from left to right, on the y-axis from bottom to top, and on the z-axis from near to far. Azimuths are measured clockwise from a given reference direction.

To use X3DAudio with right-handed coordinates, you must negate the .z element of <i>OrientFront</i>, <i>OrientTop</i>, <i>Position</i>, and <i>Velocity</i>.

For user-defined distance curves, the distance field of the first point must be 0.0f and the distance field of the last point must be 1.0f.



If an emitter moves beyond a distance of (<b>CurveDistanceScaler</b> × 1.0f), the last point on the curve is used to compute the volume output level. The last point is determined by the following:



```
X3DAUDIO_DISTANCE_CURVE.pPoints[PointCount-1].DSPSetting)
```


<h3><a id="Inner_Radius_and_Inner_Radius_Angle"></a><a id="inner_radius_and_inner_radius_angle"></a><a id="INNER_RADIUS_AND_INNER_RADIUS_ANGLE"></a>Inner Radius and Inner Radius Angle</h3>
<b>InnerRadius</b> is used to specify an area of smooth transition around the origin point as a sound travels directly through, above or below the listener. Elevation is accounted for by specifying an <b>InnerRadiusAngle</b>, whereby a sound whose elevation increases or decreases, will eventually start to bleed the sound into more than just two speakers.



When Inner Radius and Inner Radius Angle are not used, emitters are audible in the two closest speakers to their current position/orientation (or, if directly on a line with one speaker's defined angle, solely from that one speaker).



Inner Radius and Inner Radius Angle have no effect on emitters positioned outside of the cones they describe. Inside of the cone, they will gradually cause the sound to bleed into the opposite speakers, until the sound will be equally heard in all speakers when the emitter is at the same position as (or directly above or below) the listener.


<img alt="Inner radius and inner radius angle" src="./images/x3daudio_emitter_structure.png"/>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>