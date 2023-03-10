---
UID: NF:directxcollision.BoundingFrustum.Transform(BoundingFrustum&,float,FXMVECTOR,FXMVECTOR)
title: BoundingFrustum::Transform(BoundingFrustum &,float,FXMVECTOR,FXMVECTOR)
description: Transforms the BoundingFrustum using the specified scale, rotation and translation vectors.
helpviewer_keywords: ["BoundingFrustum interface [DirectX Math Support APIs]","Transform method","BoundingFrustum.Transform","BoundingFrustum.Transform(BoundingFrustum &","float","FXMVECTOR","FXMVECTOR)","BoundingFrustum.Transform(BoundingFrustum&","float","XMVECTOR","XMVECTOR)","BoundingFrustum::Transform","BoundingFrustum::Transform(BoundingFrustum &","float","FXMVECTOR","FXMVECTOR)","Transform","Transform method [DirectX Math Support APIs]","Transform method [DirectX Math Support APIs]","BoundingFrustum interface","dxmath.boundingfrustum_transform_2"]
old-location: dxmath\boundingfrustum_transform_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxmath.BoundingFrustum.Transform(BoundingFrustum@,float,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: BoundingFrustum interface [DirectX Math Support APIs],Transform method, BoundingFrustum.Transform, BoundingFrustum.Transform(BoundingFrustum &,float,FXMVECTOR,FXMVECTOR), BoundingFrustum.Transform(BoundingFrustum&,float,XMVECTOR,XMVECTOR), BoundingFrustum::Transform, BoundingFrustum::Transform(BoundingFrustum &,float,FXMVECTOR,FXMVECTOR), Transform, Transform method [DirectX Math Support APIs], Transform method [DirectX Math Support APIs],BoundingFrustum interface, dxmath.boundingfrustum_transform_2
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
 - BoundingFrustum::Transform
 - directxcollision/BoundingFrustum::Transform
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
 - BoundingFrustum.Transform
---

# BoundingFrustum::Transform(BoundingFrustum &,float,FXMVECTOR,FXMVECTOR)


## -description

Transforms the [BoundingFrustum](./ns-directxcollision-boundingfrustum.md) using the specified scale, rotation and translation vectors.

## -parameters

### -param Out [out, ref]

The transformed [BoundingFrustum](./ns-directxcollision-boundingfrustum.md).

### -param Scale [in]

The value to scale the [BoundingFrustum](./ns-directxcollision-boundingfrustum.md) by.

### -param Rotation [in]

The value to rotate the [BoundingFrustum](./ns-directxcollision-boundingfrustum.md) by.

### -param Translation [in]

The value to translate the [BoundingFrustum](./ns-directxcollision-boundingfrustum.md) by.

## -returns

This method does not return a value.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[BoundingFrustum](./ns-directxcollision-boundingfrustum.md)



<b>Reference</b>



<a href="https://msdn.microsoft.com/fba8da18-1c2e-4231-9d03-1409c733f8c7">Transform</a>