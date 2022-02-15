---
UID: NF:directxcollision.BoundingBox.CreateMerged
title: BoundingBox::CreateMerged
description: Creates a BoundingBox large enough to contains two specified BoundBox instances.
helpviewer_keywords: ["BoundingBox interface [DirectX Math Support APIs]","CreateMerged method","BoundingBox.CreateMerged","BoundingBox::CreateMerged","CreateMerged","CreateMerged method [DirectX Math Support APIs]","CreateMerged method [DirectX Math Support APIs]","BoundingBox interface","Use DirectX..BoundingBox.CreateMerged","Use DirectX::::BoundingBox::CreateMerged","dxmath.boundingbox_createmerged"]
old-location: dxmath\boundingbox_createmerged.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxcollision.BoundingBox.CreateMerged(BoundingBox@,BoundingBox,BoundingBox)
ms.date: 12/05/2018
ms.keywords: BoundingBox interface [DirectX Math Support APIs],CreateMerged method, BoundingBox.CreateMerged, BoundingBox::CreateMerged, CreateMerged, CreateMerged method [DirectX Math Support APIs], CreateMerged method [DirectX Math Support APIs],BoundingBox interface, Use DirectX..BoundingBox.CreateMerged, Use DirectX::::BoundingBox::CreateMerged, dxmath.boundingbox_createmerged
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
 - BoundingBox::CreateMerged
 - directxcollision/BoundingBox::CreateMerged
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
 - BoundingBox.CreateMerged
---

# BoundingBox::CreateMerged


## -description

Creates a BoundingBox large enough to contains two specified BoundBox instances.

## -parameters

### -param Out [out, ref]

The merged BoundingBox.

### -param b1 [in, ref]

A BoundingBox that should be contained in the new BoundingBox.

### -param b2 [in, ref]

A vector describing the plane.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[BoundingBox](./ns-directxcollision-boundingbox.md)



<a href="https://msdn.microsoft.com/68db5936-f0f8-4dbd-a183-b6c3089af0f0">Methods</a>



<b>Reference</b>