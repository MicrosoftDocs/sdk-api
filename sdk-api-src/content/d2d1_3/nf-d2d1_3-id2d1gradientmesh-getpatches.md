---
UID: NF:d2d1_3.ID2D1GradientMesh.GetPatches
title: ID2D1GradientMesh::GetPatches (d2d1_3.h)
description: Returns a subset of the patches that make up this gradient mesh.
helpviewer_keywords: ["GetPatches","GetPatches method [Direct2D]","GetPatches method [Direct2D]","ID2D1GradientMesh interface","ID2D1GradientMesh interface [Direct2D]","GetPatches method","ID2D1GradientMesh.GetPatches","ID2D1GradientMesh::GetPatches","d2d1_3/ID2D1GradientMesh::GetPatches","direct2d.id2d1gradientmesh_getpatches"]
old-location: direct2d\id2d1gradientmesh_getpatches.htm
tech.root: Direct2D
ms.assetid: d3ef9370-fb9f-d55b-d910-7dd938ecf0b6
ms.date: 12/05/2018
ms.keywords: GetPatches, GetPatches method [Direct2D], GetPatches method [Direct2D],ID2D1GradientMesh interface, ID2D1GradientMesh interface [Direct2D],GetPatches method, ID2D1GradientMesh.GetPatches, ID2D1GradientMesh::GetPatches, d2d1_3/ID2D1GradientMesh::GetPatches, direct2d.id2d1gradientmesh_getpatches
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
 - ID2D1GradientMesh::GetPatches
 - d2d1_3/ID2D1GradientMesh::GetPatches
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
 - ID2D1GradientMesh.GetPatches
---

# ID2D1GradientMesh::GetPatches


## -description

Returns a subset of the patches that make up this gradient mesh.

## -parameters

### -param startIndex

Type: <b>UINT32</b>

Index of the first patch to return.

### -param patches

Type: <b><a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch">D2D1_GRADIENT_MESH_PATCH</a>*</b>

A pointer to the array to be filled with the patch data.

### -param patchesCount

Type: <b>UINT32</b>

The number of patches to be returned.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

S_OK if successful, otherwise a failure HRESULT.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1gradientmesh">ID2D1GradientMesh</a>