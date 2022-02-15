---
UID: NF:directxmath.XMQuaternionRotationRollPitchYaw
title: XMQuaternionRotationRollPitchYaw function (directxmath.h)
description: Computes a rotation quaternion based on the pitch, yaw, and roll (Euler angles).
helpviewer_keywords: ["Use DirectX..XMQuaternionRotationRollPitchYaw","XMQuaternionRotationRollPitchYaw","XMQuaternionRotationRollPitchYaw method [DirectX Math Support APIs]","dxmath.xmquaternionrotationrollpitchyaw"]
old-location: dxmath\xmquaternionrotationrollpitchyaw.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.quaternion.XMQuaternionRotationRollPitchYaw(float,float,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMQuaternionRotationRollPitchYaw, XMQuaternionRotationRollPitchYaw, XMQuaternionRotationRollPitchYaw method [DirectX Math Support APIs], dxmath.xmquaternionrotationrollpitchyaw
req.header: directxmath.h
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
req.namespace: Use DirectX.
req.assembly:
req.type-library:
req.lib:
req.dll:
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
 - XMQuaternionRotationRollPitchYaw
 - directxmath/XMQuaternionRotationRollPitchYaw
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMQuaternionRotationRollPitchYaw
---

# XMQuaternionRotationRollPitchYaw function


## -description

Computes a rotation quaternion based on the pitch, yaw, and roll (Euler angles).

## -parameters

### -param Pitch [in]

Angle of rotation around the x-axis, in radians.

### -param Yaw [in]

Angle of rotation around the y-axis, in radians.

### -param Roll [in]

Angle of rotation around the z-axis, in radians.

## -returns

Returns the rotation quaternion.

## -remarks

The DirectXMath quaternion functions use an XMVECTOR 4-vector to represent quaternions, where the X, Y, and Z components are the vector part and the W component is the scalar part.

Angles are measured clockwise when looking along the rotation axis toward the origin. This is a left-handed coordinate system. To use right-handed coordinates, negate all three angles.

The order of transformations is roll first, then pitch, then yaw. The rotations are all applied in the global coordinate frame.

> This function takes x-axis, y-axis, z-axis angles as input parameters. The assignment of the labels *pitch* to the x-axis, *yaw* to the y-axis, and *roll* to the z-axis is a common one for computer graphics and games as it matches typical 'view' coordinate systems. There are of course other ways to assign those labels when using other coordinate systems (i.e. *roll* could be the x-axis, *pitch* the y-axis, and *yaw* the z-axis).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-quaternion">DirectXMath Library Quaternion Functions</a>
