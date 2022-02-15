---
UID: NF:directxcollision.Intersects~r1
title: Intersects
description: Test whether two triangles intersect.
tech.root: dxmath
helpviewer_keywords: ["Intersects"]
ms.date: 04/22/2019
ms.keywords: Intersects
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: directxcollision.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - Intersects
 - directxcollision/Intersects
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - directxcollision.h
api_name:
 - Intersects
---

# Intersects(XMVECTOR, XMVECTOR, XMVECTOR, XMVECTOR, XMVECTOR, XMVECTOR) method


## -description

Test whether two triangles intersect.

## -parameters

### -param A0

A vector defining triangle A.

### -param A1

A vector defining triangle A.

### -param A2

A vector defining triangle A.

### -param B0

A vector defining triangle B.

### -param B1

A vector defining triangle B.

### -param B2

A vector defining triangle B.

## -returns

A boolean value indicating whether the triangles intersect.

## -remarks

Typically the six planes passed to this function represent a frustum.

**Note**  `TriangleTests::Intersects` is new for DirectXMath. This functionality is not available in XNAMath 2.x.
Similar functionality for XNAMath can be found in the DirectX SDK Collision sample.

### Platform Requirements

Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.
Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[DirectXMath Triangle Test Functions](/windows/desktop/dxmath/ovw-xnamath-triangletests)

