---
UID: NF:directxcollision.BoundingFrustum.Contains(constBoundingSphere&)
title: BoundingFrustum::Contains(const BoundingSphere &)
description: Tests whether the BoundingFrustum contains the specified BoundingSphere.
helpviewer_keywords: ["BoundingFrustum interface [DirectX Math Support APIs]","Contains method","BoundingFrustum.Contains","BoundingFrustum.Contains(const BoundingSphere &)","BoundingFrustum.Contains(const BoundingSphere&)","BoundingFrustum::Contains","BoundingFrustum::Contains(const BoundingSphere &)","Contains","Contains method [DirectX Math Support APIs]","Contains method [DirectX Math Support APIs]","BoundingFrustum interface","dxmath.boundingfrustum_contains_5"]
old-location: dxmath\boundingfrustum_contains_5.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxmath.BoundingFrustum.Contains(BoundingSphere)
ms.date: 12/05/2018
ms.keywords: BoundingFrustum interface [DirectX Math Support APIs],Contains method, BoundingFrustum.Contains, BoundingFrustum.Contains(const BoundingSphere &), BoundingFrustum.Contains(const BoundingSphere&), BoundingFrustum::Contains, BoundingFrustum::Contains(const BoundingSphere &), Contains, Contains method [DirectX Math Support APIs], Contains method [DirectX Math Support APIs],BoundingFrustum interface, dxmath.boundingfrustum_contains_5
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
 - BoundingFrustum::Contains
 - directxcollision/BoundingFrustum::Contains
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
 - BoundingFrustum.Contains
---

# BoundingFrustum::Contains(const BoundingSphere &)


## -description

Tests whether the [BoundingFrustum](./ns-directxcollision-boundingfrustum.md) contains the specified [BoundingSphere](./ns-directxcollision-boundingsphere.md).

## -parameters

### -param sp [in, ref]

The [BoundingSphere](./ns-directxcollision-boundingsphere.md) to test against.

## -returns

A <a href="/windows/win32/api/directxcollision/ne-directxcollision-containmenttype">ContainmentType</a> value indicating whether the [BoundingSphere](./ns-directxcollision-boundingsphere.md) is contained in the [BoundingFrustum](./ns-directxcollision-boundingfrustum.md).

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[BoundingFrustum](./ns-directxcollision-boundingfrustum.md)



<a href="https://msdn.microsoft.com/b75bff54-710e-4474-9953-444970a78853">Contains</a>



<b>Reference</b>
