---
UID: NF:directxcollision.BoundingOrientedBox.ContainedBy
title: BoundingOrientedBox::ContainedBy
description: Tests whether the BoundingOrientedBox is contained by a frustum.
helpviewer_keywords: ["BoundingOrientedBox interface [DirectX Math Support APIs]","ContainedBy method","BoundingOrientedBox.ContainedBy","BoundingOrientedBox::ContainedBy","ContainedBy","ContainedBy method [DirectX Math Support APIs]","ContainedBy method [DirectX Math Support APIs]","BoundingOrientedBox interface","dxmath.boundingorientedbox_containedby"]
old-location: dxmath\boundingorientedbox_containedby.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxmath.BoundingOrientedBox.ContainedBy(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: BoundingOrientedBox interface [DirectX Math Support APIs],ContainedBy method, BoundingOrientedBox.ContainedBy, BoundingOrientedBox::ContainedBy, ContainedBy, ContainedBy method [DirectX Math Support APIs], ContainedBy method [DirectX Math Support APIs],BoundingOrientedBox interface, dxmath.boundingorientedbox_containedby
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
 - BoundingOrientedBox::ContainedBy
 - directxcollision/BoundingOrientedBox::ContainedBy
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
 - BoundingOrientedBox.ContainedBy
---

# BoundingOrientedBox::ContainedBy


## -description

Tests whether the <a href="/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox">BoundingOrientedBox</a> is contained by a frustum.

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

A <a href="/windows/win32/api/directxcollision/ne-directxcollision-containmenttype">ContainmentType</a> indicating whether the frustum contains the <a href="/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox">BoundingOrientedBox</a>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox">BoundingOrientedBox</a>



<a href="https://msdn.microsoft.com/98aa4c21-2dac-4e7a-95ef-ca87fb5e5082">Methods</a>



<b>Reference</b>

