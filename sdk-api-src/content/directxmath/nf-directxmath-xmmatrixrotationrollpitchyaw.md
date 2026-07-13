---
UID: NF:directxmath.XMMatrixRotationRollPitchYaw
title: XMMatrixRotationRollPitchYaw function (directxmath.h)
description: Builds a rotation matrix based on a given pitch, yaw, and roll (Euler angles).
helpviewer_keywords: ["Use DirectX..XMMatrixRotationRollPitchYaw","XMMatrixRotationRollPitchYaw","XMMatrixRotationRollPitchYaw method [DirectX Math Support APIs]","dxmath.xmmatrixrotationrollpitchyaw"]
old-location: dxmath\xmmatrixrotationrollpitchyaw.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixRotationRollPitchYaw(float,float,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMatrixRotationRollPitchYaw, XMMatrixRotationRollPitchYaw, XMMatrixRotationRollPitchYaw method [DirectX Math Support APIs], dxmath.xmmatrixrotationrollpitchyaw
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
 - XMMatrixRotationRollPitchYaw
 - directxmath/XMMatrixRotationRollPitchYaw
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
 - XMMatrixRotationRollPitchYaw
---

# XMMatrixRotationRollPitchYaw function


## -description

Builds a rotation matrix based on a given pitch, yaw, and roll (Euler angles).

## -parameters

### -param Pitch [in]

Angle of rotation around the x-axis, in radians.

### -param Yaw [in]

Angle of rotation around the y-axis, in radians.

### -param Roll [in]

Angle of rotation around the z-axis, in radians.

## -returns

Returns the rotation matrix.

## -remarks

Angles are measured clockwise when looking along the rotation axis toward the origin. This is a left-handed coordinate system. To use right-handed coordinates, negate all three angles.

The order of transformations is roll first, then pitch, and then yaw. The rotations are all applied in the global coordinate frame.

> [!NOTE]
> This function takes x-axis, y-axis, and z-axis angles as input parameters. The assignment of the labels *pitch* to the x-axis, *yaw* to the y-axis, and *roll* to the z-axis is a common one for computer graphics and games, since it matches typical 'view' coordinate systems. There are of course other ways to assign those labels when using other coordinate systems (for example, *roll* could be the x-axis, *pitch* the y-axis, and *yaw* the z-axis).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>
