---
UID: NF:directxmath.XMMatrixRotationRollPitchYaw
title: XMMatrixRotationRollPitchYaw function
author: windows-sdk-content
description: Builds a rotation matrix based on a given pitch, yaw, and roll (Euler angles).
old-location: dxmath\xmmatrixrotationrollpitchyaw.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixRotationRollPitchYaw(float,float,float)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMMatrixRotationRollPitchYaw, XMMatrixRotationRollPitchYaw, XMMatrixRotationRollPitchYaw method [DirectX Math Support APIs], dxmath.xmmatrixrotationrollpitchyaw
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - XMMatrixRotationRollPitchYaw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMMatrixRotationRollPitchYaw
: 
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

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d59d0dcc-deae-3f7e-55c5-0c5ff383343b">DirectXMath Library Matrix Functions</a>
 

 

