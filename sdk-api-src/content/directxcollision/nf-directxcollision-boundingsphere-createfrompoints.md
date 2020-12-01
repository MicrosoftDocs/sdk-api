---
UID: NF:directxcollision.BoundingSphere.CreateFromPoints
title: BoundingSphere::CreateFromPoints
description: Creates a new BoundingSphere from a list of points.
helpviewer_keywords: ["BoundingSphere interface [DirectX Math Support APIs]","CreateFromPoints method","BoundingSphere.CreateFromPoints","BoundingSphere::CreateFromPoints","CreateFromPoints","CreateFromPoints method [DirectX Math Support APIs]","CreateFromPoints method [DirectX Math Support APIs]","BoundingSphere interface","Use DirectX..BoundingSphere.CreateFromPoints","Use DirectX::::BoundingSphere::CreateFromPoints","dxmath.boundingsphere_createfrompoints"]
old-location: dxmath\boundingsphere_createfrompoints.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxcollision.BoundingSphere.CreateFromPoints(BoundingSphere@,size_t,XMFLOAT3,size_t)
ms.date: 12/05/2018
ms.keywords: BoundingSphere interface [DirectX Math Support APIs],CreateFromPoints method, BoundingSphere.CreateFromPoints, BoundingSphere::CreateFromPoints, CreateFromPoints, CreateFromPoints method [DirectX Math Support APIs], CreateFromPoints method [DirectX Math Support APIs],BoundingSphere interface, Use DirectX..BoundingSphere.CreateFromPoints, Use DirectX::::BoundingSphere::CreateFromPoints, dxmath.boundingsphere_createfrompoints
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
ms.custom: 19H1
f1_keywords:
 - BoundingSphere::CreateFromPoints
 - directxcollision/BoundingSphere::CreateFromPoints
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
 - BoundingSphere.CreateFromPoints
---

# BoundingSphere::CreateFromPoints


## -description

Creates a new BoundingSphere from a list of points.

## -parameters

### -param Out [out, ref]

The new BoundingSphere containing the specified points.

### -param Count [in]

The number of points in the buffer in <i>pPoints</i>.

### -param pPoints

A buffer containing the points to create the new BoundingSphere from.

### -param Stride [in]

The stride of the buffer.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[BoundingSphere](./ns-directxcollision-boundingsphere.md)



<a href="https://msdn.microsoft.com/28E771F0-B18F-459D-99C5-ABC43869A15A">Methods</a>



<b>Reference</b>