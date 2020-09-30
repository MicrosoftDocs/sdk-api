---
UID: NF:directxcollision.BoundingOrientedBox.Contains(constBoundingFrustum&)
title: BoundingOrientedBox::Contains(const BoundingFrustum &)
description: Tests whether the BoundingOrientedBox contains a BoundingFrustum.
helpviewer_keywords: ["BoundingOrientedBox interface [DirectX Math Support APIs]","Contains method","BoundingOrientedBox.Contains","BoundingOrientedBox.Contains(const BoundingFrustum &)","BoundingOrientedBox.Contains(const BoundingFrustum&)","BoundingOrientedBox.Contains","BoundingOrientedBox::Contains(const BoundingFrustum &)","BoundingOrientedBox::Contains","BoundingOrientedBox::Contains(const BoundingFrustum &)","Contains","Contains method [DirectX Math Support APIs]","Contains method [DirectX Math Support APIs]","BoundingOrientedBox interface","dxmath.boundingorientedbox_contains_1"]
old-location: dxmath\boundingorientedbox_contains_1.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxmath.BoundingOrientedBox.Contains(BoundingFrustum)
ms.date: 12/05/2018
ms.keywords: BoundingOrientedBox interface [DirectX Math Support APIs],Contains method, BoundingOrientedBox.Contains, BoundingOrientedBox.Contains(const BoundingFrustum &), BoundingOrientedBox.Contains(const BoundingFrustum&), BoundingOrientedBox.Contains,BoundingOrientedBox::Contains(const BoundingFrustum &), BoundingOrientedBox::Contains, BoundingOrientedBox::Contains(const BoundingFrustum &), Contains, Contains method [DirectX Math Support APIs], Contains method [DirectX Math Support APIs],BoundingOrientedBox interface, dxmath.boundingorientedbox_contains_1
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
 - BoundingOrientedBox::Contains
 - directxcollision/BoundingOrientedBox::Contains
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
 - BoundingOrientedBox.Contains
---

# BoundingOrientedBox::Contains(const BoundingFrustum &)


## -description

Tests whether the <a href="https://msdn.microsoft.com/ee1934f3-25ac-4a0e-84b9-6afcbdbef1f3">BoundingOrientedBox</a> contains a [BoundingFrustum](./ns-directxcollision-boundingfrustum.md).

## -parameters

### -param fr [in, ref]

The [BoundingFrustum](./ns-directxcollision-boundingfrustum.md) to test against.

## -returns

A <a href="https://msdn.microsoft.com/edc456b5-2d68-4d4e-953b-6081ad7f663c">ContainmentType</a> indicating whether the [BoundingFrustum](./ns-directxcollision-boundingfrustum.md) is contained in the <a href="https://msdn.microsoft.com/ee1934f3-25ac-4a0e-84b9-6afcbdbef1f3">BoundingOrientedBox</a>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="https://msdn.microsoft.com/ee1934f3-25ac-4a0e-84b9-6afcbdbef1f3">BoundingOrientedBox</a>



<a href="https://msdn.microsoft.com/e3df5999-021e-4360-901f-7c8790d6d12d">Contains</a>



<b>Reference</b>