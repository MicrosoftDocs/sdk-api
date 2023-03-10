---
UID: NF:directxcollision.BoundingBox.ContainedBy
title: BoundingBox::ContainedBy
description: Tests whether the BoundingBox is contained by the specified frustum.
helpviewer_keywords: ["BoundingBox interface [DirectX Math Support APIs]","ContainedBy method","BoundingBox.ContainedBy","BoundingBox::ContainedBy","ContainedBy","ContainedBy method [DirectX Math Support APIs]","ContainedBy method [DirectX Math Support APIs]","BoundingBox interface","dxmath.boundingbox_containedby"]
old-location: dxmath\boundingbox_containedby.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxcollision.BoundingBox.ContainedBy(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: BoundingBox interface [DirectX Math Support APIs],ContainedBy method, BoundingBox.ContainedBy, BoundingBox::ContainedBy, ContainedBy, ContainedBy method [DirectX Math Support APIs], ContainedBy method [DirectX Math Support APIs],BoundingBox interface, dxmath.boundingbox_containedby
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
ms.custom: 19H1
f1_keywords:
 - BoundingBox::ContainedBy
 - directxcollision/BoundingBox::ContainedBy
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
 - BoundingBox.ContainedBy
---

# BoundingBox::ContainedBy


## -description

Tests whether the [BoundingBox](./ns-directxcollision-boundingbox.md) is contained by the specified frustum.

## -parameters

### -param Plane0 [in]

A plane describing the frustum.

### -param Plane1 [in]

A plane describing the frustum.

### -param Plane2 [in]

A plane describing the frustum.

### -param Plane3 [in]

A plane describing the frustum.

### -param Plane4 [in]

A plane describing the frustum.

### -param Plane5 [in]

A plane describing the frustum.

## -returns

A <a href="/windows/win32/api/directxcollision/ne-directxcollision-containmenttype">ContainmentType</a> value indicating whether the frustum contains the [BoundingBox](./ns-directxcollision-boundingbox.md).

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[BoundingBox](./ns-directxcollision-boundingbox.md)



<a href="https://msdn.microsoft.com/68db5936-f0f8-4dbd-a183-b6c3089af0f0">Methods</a>



<b>Reference</b>
