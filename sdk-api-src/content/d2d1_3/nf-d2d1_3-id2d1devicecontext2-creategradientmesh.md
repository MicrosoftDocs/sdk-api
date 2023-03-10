---
UID: NF:d2d1_3.ID2D1DeviceContext2.CreateGradientMesh
title: ID2D1DeviceContext2::CreateGradientMesh (d2d1_3.h)
description: Creates a new ID2D1GradientMesh instance using the given array of patches.
helpviewer_keywords: ["CreateGradientMesh","CreateGradientMesh method [Direct2D]","CreateGradientMesh method [Direct2D]","ID2D1DeviceContext2 interface","ID2D1DeviceContext2 interface [Direct2D]","CreateGradientMesh method","ID2D1DeviceContext2.CreateGradientMesh","ID2D1DeviceContext2::CreateGradientMesh","d2d1_3/ID2D1DeviceContext2::CreateGradientMesh","direct2d.id2d1devicecontext2_creategradientmesh"]
old-location: direct2d\id2d1devicecontext2_creategradientmesh.htm
tech.root: Direct2D
ms.assetid: 7c471ba3-fb0f-b735-d10b-9d0a56b32863
ms.date: 12/05/2018
ms.keywords: CreateGradientMesh, CreateGradientMesh method [Direct2D], CreateGradientMesh method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],CreateGradientMesh method, ID2D1DeviceContext2.CreateGradientMesh, ID2D1DeviceContext2::CreateGradientMesh, d2d1_3/ID2D1DeviceContext2::CreateGradientMesh, direct2d.id2d1devicecontext2_creategradientmesh
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
 - ID2D1DeviceContext2::CreateGradientMesh
 - d2d1_3/ID2D1DeviceContext2::CreateGradientMesh
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
 - ID2D1DeviceContext2.CreateGradientMesh
---

# ID2D1DeviceContext2::CreateGradientMesh


## -description

Creates a new <a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1gradientmesh">ID2D1GradientMesh</a> instance using the given array of patches.

## -parameters

### -param patches [in]

Type: <b>const <a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch">D2D1_GRADIENT_MESH_PATCH</a>*</b>

A pointer to the array containing the patches to be used in this mesh.

### -param patchesCount

Type: <b>UINT32</b>

The number of patches in the patches argument to read.

### -param gradientMesh [out]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1gradientmesh">ID2D1GradientMesh</a>**</b>

When this method returns, contains the address of a pointer to the new gradient mesh.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

S_OK if successful, otherwise a failure HRESULT.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2">ID2D1DeviceContext2</a>