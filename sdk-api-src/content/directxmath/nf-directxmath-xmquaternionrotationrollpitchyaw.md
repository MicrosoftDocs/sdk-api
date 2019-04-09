---
UID: NF:directxmath.XMQuaternionRotationRollPitchYaw
title: XMQuaternionRotationRollPitchYaw function (directxmath.h)
author: windows-sdk-content
description: Computes a rotation quaternion based on the pitch, yaw, and roll (Euler angles).
old-location: dxmath\xmquaternionrotationrollpitchyaw.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.quaternion.XMQuaternionRotationRollPitchYaw(float,float,float)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMQuaternionRotationRollPitchYaw, XMQuaternionRotationRollPitchYaw, XMQuaternionRotationRollPitchYaw method [DirectX Math Support APIs], dxmath.xmquaternionrotationrollpitchyaw
ms.topic: function
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
 - XMQuaternionRotationRollPitchYaw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



The DirectXMath quaternion functions use an XMVECTOR 4-vector to represent quaternions, 
    where the X, Y, and Z components are the vector part and the W component is the scalar part.

Angles are measured clockwise when looking along the rotation axis toward the origin. This is a left-handed coordinate system. To use right-handed coordinates, negate all three angles.

The order of transformations is roll first, then pitch, then yaw. The rotations are all applied in the global coordinate
   frame.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/2d397c98-d0cd-08e0-6104-cca31bb6bd11">DirectXMath Library Quaternion Functions</a>
 

 

