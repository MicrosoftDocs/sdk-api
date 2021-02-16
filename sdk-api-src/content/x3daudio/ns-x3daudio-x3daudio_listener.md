---
UID: NS:x3daudio.X3DAUDIO_LISTENER
title: X3DAUDIO_LISTENER (x3daudio.h)
description: Defines a point of 3D audio reception.
helpviewer_keywords: ["*LPX3DAUDIO_LISTENER","LPX3DAUDIO_LISTENER","LPX3DAUDIO_LISTENER structure pointer [XAudio2 Audio Mixing APIs]","X3DAUDIO_LISTENER","X3DAUDIO_LISTENER structure [XAudio2 Audio Mixing APIs]","x3daudio/LPX3DAUDIO_LISTENER","x3daudio/X3DAUDIO_LISTENER","xaudio2.x3daudio_listener"]
old-location: xaudio2\x3daudio_listener.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.x3daudio.X3DAUDIO_LISTENER
ms.date: 12/05/2018
ms.keywords: '*LPX3DAUDIO_LISTENER, LPX3DAUDIO_LISTENER, LPX3DAUDIO_LISTENER structure pointer [XAudio2 Audio Mixing APIs], X3DAUDIO_LISTENER, X3DAUDIO_LISTENER structure [XAudio2 Audio Mixing APIs], x3daudio/LPX3DAUDIO_LISTENER, x3daudio/X3DAUDIO_LISTENER, xaudio2.x3daudio_listener'
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
req.typenames: X3DAUDIO_LISTENER, *LPX3DAUDIO_LISTENER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X3DAUDIO_LISTENER
 - x3daudio/X3DAUDIO_LISTENER
 - LPX3DAUDIO_LISTENER
 - x3daudio/LPX3DAUDIO_LISTENER
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
 - X3DAUDIO_LISTENER
---

# X3DAUDIO_LISTENER structure


## -description

Defines a point of 3D audio reception.

## -struct-fields

### -field OrientFront

Orientation of front direction. When <b>pCone</b> is NULL <b>OrientFront</b> is used only for matrix and delay calculations. When <b>pCone</b> is not NULL <b>OrientFront</b> is used for matrix, LPF (both direct and reverb paths), and reverb calculations. This value must be orthonormal with <b>OrientTop</b> when used.

### -field OrientTop

Orientation of top direction, used only for matrix and delay calculations. This value must be orthonormal with <b>OrientFront</b> when used.

### -field Position

Position in user-defined world units. This value does not affect <b>Velocity</b>.

### -field Velocity

Velocity vector in user-defined world units per second, used only for doppler calculations. This value does not affect <b>Position</b>.

### -field pCone

Pointer to an <a href="/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone">X3DAUDIO_CONE</a> structure for this listener. Providing a listener cone will specify that additional calculations are performed when determining the volume and filter DSP parameters for individual sound sources. A NULL <b>pCone</b> value specifies an omnidirectional sound and no cone processing is applied. <b>pCone</b> is only used for matrix, LPF (both direct and reverb paths), and reverb calculations.

## -remarks

X3DAudio uses a left-handed Cartesian coordinate system, with values on the x-axis increasing from left to right, on the y-axis from bottom to top, and on the z-axis from near to far. Azimuths are measured clockwise from a given reference direction.

To use X3DAudio with right-handed coordinates, you must negate the .z element of <i>OrientFront</i>, <i>OrientTop</i>, <i>Position</i>, and <i>Velocity</i>.

The parameter type <b>X3DAUDIO_VECTOR</b> is typed to DirectX::XMFLOAT3, to provide x, y and z floating-point values.



A listener's front and top vectors must be orthonormal. To be considered orthonormal, a pair of vectors must have a magnitude of 1 +- 1x10-5 and a dot product of 0 +- 1x10-5.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)