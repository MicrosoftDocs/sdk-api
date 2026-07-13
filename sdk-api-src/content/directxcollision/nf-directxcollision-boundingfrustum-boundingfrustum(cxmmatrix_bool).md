---
UID: NF:directxcollision.BoundingFrustum.BoundingFrustum(CXMMATRIX,bool)
title: BoundingFrustum::BoundingFrustum(CXMMATRIX,bool)
description: Creates an instance of BoundingFrustum from a left-handed projection matrix.
tech.root: dxmath
ms.date: 06/24/2021
req.construct-type: function
req.header: directxcollision.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
 - BoundingFrustum::BoundingFrustum
 - directxcollision/BoundingFrustum::BoundingFrustum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxcollision.h
api_name:
 - BoundingFrustum::BoundingFrustum
---

## -description

Creates an instance of [BoundingFrustum](./ns-directxcollision-boundingfrustum.md) from a left-handed projection matrix.For more info, see <a href="/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-createfrommatrix">BoundingFrustum::CreateFromMatrix</a>.

## -parameters

### -param Projection

The left-handed projection matrix to create the frustum from.

### -param rhcoords

`true` for a right-hand coordinate system; otherwise, `false`.

## -returns

## -remarks

## -see-also

* [BoundingFrustum](ns-directxcollision-boundingfrustum.md)
