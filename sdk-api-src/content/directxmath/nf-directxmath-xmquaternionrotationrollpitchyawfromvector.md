---
UID: NF:directxmath.XMQuaternionRotationRollPitchYawFromVector
title: XMQuaternionRotationRollPitchYawFromVector function (directxmath.h)
author: windows-sdk-content
description: Computes a rotation quaternion based on a vector containing the Euler angles (pitch, yaw, and roll).
old-location: dxmath\xmquaternionrotationrollpitchyawfromvector.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.quaternion.XMQuaternionRotationRollPitchYawFromVector(XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMQuaternionRotationRollPitchYawFromVector, XMQuaternionRotationRollPitchYawFromVector, XMQuaternionRotationRollPitchYawFromVector method [DirectX Math Support APIs], dxmath.xmquaternionrotationrollpitchyawfromvector
ms.topic: function
f1_keywords: 
 - "directxmath/XMQuaternionRotationRollPitchYawFromVector"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMQuaternionRotationRollPitchYawFromVector
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMQuaternionRotationRollPitchYawFromVector function


## -description


Computes a rotation quaternion based on a vector containing the Euler angles (pitch, yaw, and roll).


## -parameters




### -param Angles [in]

3D vector containing the Euler angles in the order pitch, yaw, roll.


## -returns



Returns the rotation quaternion.




## -remarks



The DirectXMath quaternion functions use an XMVECTOR 4-vector to represent quaternions, 
    where the X, Y, and Z components are the vector part and the W component is the scalar part.

Angles are measured clockwise when looking along the rotation axis toward the origin. This is a left-handed coordinate system. To use right-handed coordinates, negate all three angles.

The order of transformations is roll first, then pitch, then yaw. The rotations are all applied in the global coordinate
   frame.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-quaternion">DirectXMath Library Quaternion Functions</a>
 

 

