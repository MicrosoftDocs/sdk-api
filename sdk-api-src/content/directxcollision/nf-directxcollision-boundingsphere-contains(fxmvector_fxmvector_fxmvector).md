---
UID: NF:directxcollision.BoundingSphere.Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR)
title: BoundingSphere::Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR)
description: Tests whether the BoundingSphere contains a specified triangle.
helpviewer_keywords: ["BoundingSphere interface [DirectX Math Support APIs]","Contains method","BoundingSphere.Contains","BoundingSphere.Contains(FXMVECTOR","FXMVECTOR","FXMVECTOR)","BoundingSphere.Contains(XMVECTOR","XMVECTOR","XMVECTOR)","BoundingSphere::Contains","BoundingSphere::Contains(FXMVECTOR","FXMVECTOR","FXMVECTOR)","Contains","Contains method [DirectX Math Support APIs]","Contains method [DirectX Math Support APIs]","BoundingSphere interface","dxmath.boundingsphere_contains_2"]
old-location: dxmath\boundingsphere_contains_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxcollision.BoundingSphere.Contains(XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: BoundingSphere interface [DirectX Math Support APIs],Contains method, BoundingSphere.Contains, BoundingSphere.Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR), BoundingSphere.Contains(XMVECTOR,XMVECTOR,XMVECTOR), BoundingSphere::Contains, BoundingSphere::Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR), Contains, Contains method [DirectX Math Support APIs], Contains method [DirectX Math Support APIs],BoundingSphere interface, dxmath.boundingsphere_contains_2
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

# BoundingSphere::Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR)


## -description

Tests whether the BoundingSphere contains a specified triangle.

## -parameters

### -param V0 [in]

A corner of the triangle.

### -param V1 [in]

A corner of the triangle.

### -param V2 [in]

A corner of the triangle.

## -returns

A ContainmentType value indicating whether the BoundingSphere contains the specified triangle.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[BoundingSphere](./ns-directxcollision-boundingsphere.md)



<a href="https://msdn.microsoft.com/e5e42d29-f39f-44cd-8be1-06afd5eec7d9">Contains</a>



<b>Reference</b>