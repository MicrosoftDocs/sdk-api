---
UID: NF:directxcollision.BoundingFrustum.Intersects(FXMVECTOR,FXMVECTOR,float&)
title: BoundingFrustum::Intersects(FXMVECTOR,FXMVECTOR,float &)
description: Test the BoundingFrustum for intersection with a ray.
helpviewer_keywords: ["BoundingFrustum interface [DirectX Math Support APIs]","Intersects method","BoundingFrustum.Intersects","BoundingFrustum.Intersects(FXMVECTOR","FXMVECTOR","float &)","BoundingFrustum.Intersects(XMVECTOR","XMVECTOR","float&)","BoundingFrustum::Intersects","BoundingFrustum::Intersects(FXMVECTOR","FXMVECTOR","float &)","Intersects","Intersects method [DirectX Math Support APIs]","Intersects method [DirectX Math Support APIs]","BoundingFrustum interface","dxmath.boundingfrustum_intersects_2"]
old-location: dxmath\boundingfrustum_intersects_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxmath.BoundingFrustum.Intersects(XMVECTOR,XMVECTOR,float@)
ms.date: 12/05/2018
ms.keywords: BoundingFrustum interface [DirectX Math Support APIs],Intersects method, BoundingFrustum.Intersects, BoundingFrustum.Intersects(FXMVECTOR,FXMVECTOR,float &), BoundingFrustum.Intersects(XMVECTOR,XMVECTOR,float&), BoundingFrustum::Intersects, BoundingFrustum::Intersects(FXMVECTOR,FXMVECTOR,float &), Intersects, Intersects method [DirectX Math Support APIs], Intersects method [DirectX Math Support APIs],BoundingFrustum interface, dxmath.boundingfrustum_intersects_2
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
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - BoundingFrustum::Intersects
 - directxcollision/BoundingFrustum::Intersects
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
 - BoundingFrustum.Intersects
---

## -description

Test the [BoundingFrustum](./ns-directxcollision-boundingfrustum.md) for intersection with a ray.

## -parameters

### -param rayOrigin

The origin of the ray.

### -param Direction [in]

The direction of the ray.

### -param Dist [out, ref]

The length of the ray.

## -returns

A boolean value indicating whether the [BoundingFrustum](./ns-directxcollision-boundingfrustum.md) intersects with the ray.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[BoundingFrustum](./ns-directxcollision-boundingfrustum.md)



<a href="https://msdn.microsoft.com/9e947766-5361-4cf5-8ffa-43e6bbfc98b2">Intersects</a>



<b>Reference</b>