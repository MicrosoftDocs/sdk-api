---
UID: NF:d2d1_3.ID2D1DeviceContext2.GetGradientMeshWorldBounds
title: ID2D1DeviceContext2::GetGradientMeshWorldBounds (d2d1_3.h)
description: Returns the world bounds of a given gradient mesh.
helpviewer_keywords: ["GetGradientMeshWorldBounds","GetGradientMeshWorldBounds method [Direct2D]","GetGradientMeshWorldBounds method [Direct2D]","ID2D1DeviceContext2 interface","ID2D1DeviceContext2 interface [Direct2D]","GetGradientMeshWorldBounds method","ID2D1DeviceContext2.GetGradientMeshWorldBounds","ID2D1DeviceContext2::GetGradientMeshWorldBounds","d2d1_3/ID2D1DeviceContext2::GetGradientMeshWorldBounds","direct2d.id2d1devicecontext2_getgradientmeshworldbounds"]
old-location: direct2d\id2d1devicecontext2_getgradientmeshworldbounds.htm
tech.root: Direct2D
ms.assetid: 809d851c-a3e0-7609-95e0-637e25cdaa06
ms.date: 12/05/2018
ms.keywords: GetGradientMeshWorldBounds, GetGradientMeshWorldBounds method [Direct2D], GetGradientMeshWorldBounds method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],GetGradientMeshWorldBounds method, ID2D1DeviceContext2.GetGradientMeshWorldBounds, ID2D1DeviceContext2::GetGradientMeshWorldBounds, d2d1_3/ID2D1DeviceContext2::GetGradientMeshWorldBounds, direct2d.id2d1devicecontext2_getgradientmeshworldbounds
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext2::GetGradientMeshWorldBounds
 - d2d1_3/ID2D1DeviceContext2::GetGradientMeshWorldBounds
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext2.GetGradientMeshWorldBounds
---

# ID2D1DeviceContext2::GetGradientMeshWorldBounds


## -description

Returns the world bounds of a given gradient mesh.

## -parameters

### -param gradientMesh [in]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1gradientmesh">ID2D1GradientMesh</a>*</b>

The gradient mesh whose world bounds will be calculated.

### -param pBounds [out]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

When this method returns, contains a pointer to the bounds of the gradient mesh, in device independent pixels (DIPs).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

S_OK if successful, otherwise a failure HRESULT.

## -remarks

The world bounds reflect the current DPI, unit mode, and world transform of the context. They indicate which pixels would be impacted by calling DrawGradientMesh with the given gradient mesh. 
They do not reflect the current clip rectangle set on the device context or the extent of the context’s current target.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2">ID2D1DeviceContext2</a>