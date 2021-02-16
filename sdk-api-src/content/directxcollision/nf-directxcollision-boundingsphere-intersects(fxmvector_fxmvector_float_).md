---
UID: NF:directxcollision.BoundingSphere.Intersects(FXMVECTOR,FXMVECTOR,float&)
title: BoundingSphere::Intersects(FXMVECTOR,FXMVECTOR,float &)
description: Tests the BoundingSphere for intersection with a ray.
helpviewer_keywords: ["BoundingSphere interface [DirectX Math Support APIs]","Intersects method","BoundingSphere.Intersects","BoundingSphere.Intersects(FXMVECTOR","FXMVECTOR","float &)","BoundingSphere.Intersects(XMVECTOR","XMVECTOR","float&)","BoundingSphere::Intersects","BoundingSphere::Intersects(FXMVECTOR","FXMVECTOR","float &)","Intersects","Intersects method [DirectX Math Support APIs]","Intersects method [DirectX Math Support APIs]","BoundingSphere interface","dxmath.boundingsphere_intersects_2"]
old-location: dxmath\boundingsphere_intersects_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxcollision.BoundingSphere.Intersects(XMVECTOR,XMVECTOR,float@)
ms.date: 12/05/2018
ms.keywords: BoundingSphere interface [DirectX Math Support APIs],Intersects method, BoundingSphere.Intersects, BoundingSphere.Intersects(FXMVECTOR,FXMVECTOR,float &), BoundingSphere.Intersects(XMVECTOR,XMVECTOR,float&), BoundingSphere::Intersects, BoundingSphere::Intersects(FXMVECTOR,FXMVECTOR,float &), Intersects, Intersects method [DirectX Math Support APIs], Intersects method [DirectX Math Support APIs],BoundingSphere interface, dxmath.boundingsphere_intersects_2
req.header: directxcollision.h
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
f1_keywords:
 - BoundingSphere::Intersects
 - directxcollision/BoundingSphere::Intersects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXCollision.h
api_name:
 - BoundingSphere.Intersects
---

# BoundingSphere::Intersects(FXMVECTOR,FXMVECTOR,float &)


## -description

Tests the BoundingSphere for intersection with a ray.

## -parameters

### -param Origin [in]

The origin of the ray.

### -param Direction [in]

The direction of the ray.

### -param Dist [out, ref]

The length of the ray.

## -returns

A bool value indicating whether the BoundingSphere contains the specified ray.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[BoundingSphere](./ns-directxcollision-boundingsphere.md)



<a href="https://msdn.microsoft.com/639a1eba-1868-4723-9899-507e5cfb39d7">Intersects</a>



<b>Reference</b>