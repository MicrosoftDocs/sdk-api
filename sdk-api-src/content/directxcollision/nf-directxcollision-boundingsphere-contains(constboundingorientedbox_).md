---
UID: NF:directxcollision.BoundingSphere.Contains(constBoundingOrientedBox&)
title: BoundingSphere::Contains(const BoundingOrientedBox &)
description: Tests whether the BoundingSphere contains the specified BoundingOrientedBox.
helpviewer_keywords: ["BoundingSphere interface [DirectX Math Support APIs]","Contains method","BoundingSphere.Contains","BoundingSphere.Contains(const BoundingOrientedBox &)","BoundingSphere.Contains(const BoundingOrientedBox&)","BoundingSphere::Contains","BoundingSphere::Contains(const BoundingOrientedBox &)","Contains","Contains method [DirectX Math Support APIs]","Contains method [DirectX Math Support APIs]","BoundingSphere interface","dxmath.boundingsphere_contains_4"]
old-location: dxmath\boundingsphere_contains_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxcollision.BoundingSphere.Contains(BoundingOrientedBox)
ms.date: 12/05/2018
ms.keywords: BoundingSphere interface [DirectX Math Support APIs],Contains method, BoundingSphere.Contains, BoundingSphere.Contains(const BoundingOrientedBox &), BoundingSphere.Contains(const BoundingOrientedBox&), BoundingSphere::Contains, BoundingSphere::Contains(const BoundingOrientedBox &), Contains, Contains method [DirectX Math Support APIs], Contains method [DirectX Math Support APIs],BoundingSphere interface, dxmath.boundingsphere_contains_4
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
 - BoundingSphere::Contains
 - directxcollision/BoundingSphere::Contains
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
 - BoundingSphere.Contains
---

# BoundingSphere::Contains(const BoundingOrientedBox &)


## -description

Tests whether the [BoundingSphere](./ns-directxcollision-boundingsphere.md) contains the specified <a href="https://msdn.microsoft.com/ee1934f3-25ac-4a0e-84b9-6afcbdbef1f3">BoundingOrientedBox</a>.

## -parameters

### -param box [in, ref]

The <a href="https://msdn.microsoft.com/ee1934f3-25ac-4a0e-84b9-6afcbdbef1f3">BoundingOrientedBox</a> to test against.

## -returns

A <a href="https://msdn.microsoft.com/edc456b5-2d68-4d4e-953b-6081ad7f663c">ContainmentType</a> value indicating whether the <a href="https://msdn.microsoft.com/ee1934f3-25ac-4a0e-84b9-6afcbdbef1f3">BoundingOrientedBox</a> is contained in the [BoundingSphere](./ns-directxcollision-boundingsphere.md).

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[BoundingSphere](./ns-directxcollision-boundingsphere.md)



<a href="https://msdn.microsoft.com/e5e42d29-f39f-44cd-8be1-06afd5eec7d9">Contains</a>



<b>Reference</b>