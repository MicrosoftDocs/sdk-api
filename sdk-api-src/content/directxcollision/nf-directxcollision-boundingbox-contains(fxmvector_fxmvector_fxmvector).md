---
UID: NF:directxcollision.BoundingBox.Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR)
title: BoundingBox::Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR)
description: Test whether the BoundingBox contains a specified triangle.
helpviewer_keywords: ["BoundingBox interface [DirectX Math Support APIs]","Contains method","BoundingBox.Contains","BoundingBox.Contains(FXMVECTOR","FXMVECTOR","FXMVECTOR)","BoundingBox.Contains(XMVECTOR","XMVECTOR","XMVECTOR)","BoundingBox::Contains","BoundingBox::Contains(FXMVECTOR","FXMVECTOR","FXMVECTOR)","Contains","Contains method [DirectX Math Support APIs]","Contains method [DirectX Math Support APIs]","BoundingBox interface","dxmath.boundingbox_contains_2"]
old-location: dxmath\boundingbox_contains_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxcollision.BoundingBox.Contains(XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: BoundingBox interface [DirectX Math Support APIs],Contains method, BoundingBox.Contains, BoundingBox.Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR), BoundingBox.Contains(XMVECTOR,XMVECTOR,XMVECTOR), BoundingBox::Contains, BoundingBox::Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR), Contains, Contains method [DirectX Math Support APIs], Contains method [DirectX Math Support APIs],BoundingBox interface, dxmath.boundingbox_contains_2
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
 - BoundingBox::Contains
 - directxcollision/BoundingBox::Contains
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
 - BoundingBox.Contains
---

# BoundingBox::Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR)


## -description

Test whether the BoundingBox contains a specified triangle.

## -parameters

### -param V0 [in]

A corner of the triangle.

### -param V1 [in]

A corner of the triangle.

### -param V2 [in]

A corner of the triangle.

## -returns

A ContainmentType value indicating whether the BoundingBox contains the specified triangle.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[BoundingBox](./ns-directxcollision-boundingbox.md)



<a href="https://msdn.microsoft.com/876c7764-9378-48e5-812c-3646930900c5">Contains</a>



<b>Reference</b>