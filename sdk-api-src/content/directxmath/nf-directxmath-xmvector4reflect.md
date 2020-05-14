---
UID: NF:directxmath.XMVector4Reflect
title: XMVector4Reflect function (directxmath.h)
description: Reflects an incident 4D vector across a 4D normal vector.helpviewer_keywords: ["Use DirectX..XMVector4Reflect","XMVector4Reflect","XMVector4Reflect method [DirectX Math Support APIs]","dxmath.xmvector4reflect"]
old-location: dxmath\xmvector4reflect.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector4Reflect(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector4Reflect, XMVector4Reflect, XMVector4Reflect method [DirectX Math Support APIs], dxmath.xmvector4reflect
f1_keywords:
- directxmath/XMVector4Reflect
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
- XMVector4Reflect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVector4Reflect function


## -description


Reflects an incident 4D vector across a 4D normal vector.


## -parameters




### -param Incident [in]

4D incident vector to reflect.


### -param Normal [in]

4D normal vector to reflect the incident vector across.


## -returns



Returns the reflected incident angle.




## -remarks



The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

float s = 2.0f * dot(Incident, Normal);

Result.x = Incident.x - s * Normal.x;
Result.y = Incident.y - s * Normal.y;
Result.z = Incident.z - s * Normal.z;
Result.w = Incident.w - s * Normal.w;

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector4-geometric">DirectXMath Library 4D Vector Geometric Functions</a>
 

 

