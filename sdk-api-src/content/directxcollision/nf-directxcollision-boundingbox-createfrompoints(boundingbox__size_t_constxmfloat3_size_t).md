---
UID: NF:directxcollision.BoundingBox.CreateFromPoints(BoundingBox&,size_t,constXMFLOAT3,size_t)
title: BoundingBox::CreateFromPoints(BoundingBox &,size_t,const XMFLOAT3,size_t)
description: Creates a BoundingBox from a list of points.
helpviewer_keywords: ["BoundingBox interface [DirectX Math Support APIs]","CreateFromPoints method","BoundingBox.CreateFromPoints","BoundingBox.CreateFromPoints(BoundingBox &","size_t","const XMFLOAT3","size_t)","BoundingBox.CreateFromPoints(BoundingBox&","size_t","const XMFLOAT3*","size_t)","BoundingBox::CreateFromPoints","BoundingBox::CreateFromPoints(BoundingBox &","size_t","const XMFLOAT3","size_t)","CreateFromPoints","CreateFromPoints method [DirectX Math Support APIs]","CreateFromPoints method [DirectX Math Support APIs]","BoundingBox interface","dxmath.boundingbox_createfrompoints_1"]
old-location: dxmath\boundingbox_createfrompoints_1.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxcollision.BoundingBox.CreateFromPoints(BoundingBox@,size_t,XMFLOAT3,size_t)
ms.date: 12/05/2018
ms.keywords: BoundingBox interface [DirectX Math Support APIs],CreateFromPoints method, BoundingBox.CreateFromPoints, BoundingBox.CreateFromPoints(BoundingBox &,size_t,const XMFLOAT3,size_t), BoundingBox.CreateFromPoints(BoundingBox&,size_t,const XMFLOAT3*,size_t), BoundingBox::CreateFromPoints, BoundingBox::CreateFromPoints(BoundingBox &,size_t,const XMFLOAT3,size_t), CreateFromPoints, CreateFromPoints method [DirectX Math Support APIs], CreateFromPoints method [DirectX Math Support APIs],BoundingBox interface, dxmath.boundingbox_createfrompoints_1
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
 - BoundingBox::CreateFromPoints
 - directxcollision/BoundingBox::CreateFromPoints
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
 - BoundingBox.CreateFromPoints
---

# BoundingBox::CreateFromPoints(BoundingBox &,size_t,const XMFLOAT3,size_t)


## -description

Creates a BoundingBox from a list of points.

## -parameters

### -param Out [out, ref]

The new BoundingBox containing the specified points.

### -param Count [in]

Number of points in the buffer in <i>pPoints</i>.

### -param pPoints

A buffer containing points to create the BoundingBox from.

### -param Stride [in]

The stride of the buffer.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[BoundingBox](./ns-directxcollision-boundingbox.md)



<a href="https://msdn.microsoft.com/29c5b400-ebc2-4e3e-81a0-1790a6f7b562">CreateFromPoints</a>



<b>Reference</b>