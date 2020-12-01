---
UID: NF:directxcollision.ContainedBy
title: ContainedBy function
description: Tests whether a triangle is contained within six planes (typically a frustum).
helpviewer_keywords: ["ContainedBy","ContainedBy method [DirectX Math Support APIs]","DirectX::TriangleTests.ContainedBy","dxmath.containedby"]
old-location: dxmath\containedby.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.TriangleTests.ContainedBy(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: ContainedBy, ContainedBy method [DirectX Math Support APIs], DirectX::TriangleTests.ContainedBy, dxmath.containedby
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
req.namespace: DirectX::TriangleTests
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
 - ContainedBy
 - directxcollision/ContainedBy
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
 - ContainedBy
---

# ContainedBy function


## -description

Tests whether a triangle is contained within six planes (typically a frustum).

## -parameters

### -param V0

A vector defining the triangle.

### -param V1

A vector defining the triangle.

### -param V2

A vector defining the triangle.

### -param Plane0

A vector defining a plane.

### -param Plane1

A vector defining a plane.

### -param Plane2

A vector defining a plane.

### -param Plane3

A vector defining a plane.

### -param Plane4

A vector defining a plane.

### -param Plane5

A vector defining a plane.

## -returns

A <a href="/windows/win32/api/directxcollision/ne-directxcollision-containmenttype">ContainmentType</a> value indicating whether the triangle is contained within the planes.

## -remarks

<div class="alert"><b>Note</b>  <code>TriangleTests</code>::<code>ContainedBy</code> is new for DirectXMath.  This functionality is not available in XNAMath 2.x.  
  Similar functionality for XNAMath can be found in the DirectX SDK Collision sample.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-triangletests">DirectXMath Triangle Test Functions</a>
