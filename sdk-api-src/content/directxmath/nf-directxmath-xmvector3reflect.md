---
UID: NF:directxmath.XMVector3Reflect
title: XMVector3Reflect function (directxmath.h)
description: Reflects an incident 3D vector across a 3D normal vector.helpviewer_keywords: ["Use DirectX..XMVector3Reflect","XMVector3Reflect","XMVector3Reflect method [DirectX Math Support APIs]","dxmath.xmvector3reflect"]
old-location: dxmath\xmvector3reflect.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector3Reflect(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3Reflect, XMVector3Reflect, XMVector3Reflect method [DirectX Math Support APIs], dxmath.xmvector3reflect
f1_keywords:
- directxmath/XMVector3Reflect
dev_langs:
- c++
req.header: directxmath.h
req.include-header: DirectXMath.h
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
- directxmathvector.inl
api_name:
- XMVector3Reflect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVector3Reflect function


## -description


Reflects an incident 3D vector across a 3D normal vector.


## -parameters




### -param Incident [in]

3D incident vector to reflect.


### -param Normal [in]

3D normal vector to reflect the incident vector across.


## -returns



Returns the reflected incident angle.




## -remarks



The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

float s = 2.0f * ( Incident.x * Normal.x + Incident.y * Normal.y + Incident.z * Normal.z );

Result.x = Incident.x - s * Normal.x;
Result.y = Incident.y - s * Normal.y;
Result.z = Incident.z - s * Normal.z;
Result.w = undefined;

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-geometric">DirectXMath Library 3D Vector Geometric Functions</a>
 

 

