---
UID: NS:d2d1_3.D2D1_GRADIENT_MESH_PATCH
title: D2D1_GRADIENT_MESH_PATCH (d2d1_3.h)
description: Represents a tensor patch with 16 control points, 4 corner colors, and boundary flags. An ID2D1GradientMesh is made up of 1 or more gradient mesh patches. Use the GradientMeshPatch function or the GradientMeshPatchFromCoonsPatch function to create one.
helpviewer_keywords: ["D2D1_GRADIENT_MESH_PATCH","D2D1_GRADIENT_MESH_PATCH structure [Direct2D]","d2d1_3/D2D1_GRADIENT_MESH_PATCH","direct2d.D2D1_GRADIENT_MESH_PATCH"]
old-location: direct2d\D2D1_GRADIENT_MESH_PATCH.htm
tech.root: Direct2D
ms.assetid: 16d1ef03-f0c9-7414-d54d-9513199272aa
ms.date: 12/05/2018
ms.keywords: D2D1_GRADIENT_MESH_PATCH, D2D1_GRADIENT_MESH_PATCH structure [Direct2D], d2d1_3/D2D1_GRADIENT_MESH_PATCH, direct2d.D2D1_GRADIENT_MESH_PATCH
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_GRADIENT_MESH_PATCH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_GRADIENT_MESH_PATCH
 - d2d1_3/D2D1_GRADIENT_MESH_PATCH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_3.h
api_name:
 - D2D1_GRADIENT_MESH_PATCH
---

# D2D1_GRADIENT_MESH_PATCH structure


## -description

Represents a tensor patch with 16 control points, 4 corner colors, and boundary flags. An ID2D1GradientMesh is made up of 1 or more gradient mesh patches.
          Use the <a href="/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatch">GradientMeshPatch function</a> or the <a href="/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatchfromcoonspatch">GradientMeshPatchFromCoonsPatch function</a> to create one.

## -struct-fields

### -field point00

The coordinate-space location of the control point in column 0 and row 0 of the tensor grid.

### -field point01

The coordinate-space location of the control point in column 0 and row 1 of the tensor grid.

### -field point02

The coordinate-space location of the control point in column 0 and row 2 of the tensor grid.

### -field point03

The coordinate-space location of the control point in column 0 and row 3 of the tensor grid.

### -field point10

The coordinate-space location of the control point in column 1 and row 0 of the tensor grid.

### -field point11

The coordinate-space location of the control point in column 1 and row 1 of the tensor grid.

### -field point12

The coordinate-space location of the control point in column 1 and row 2 of the tensor grid.

### -field point13

The coordinate-space location of the control point in column 1 and row 3 of the tensor grid.

### -field point20

The coordinate-space location of the control point in column 2 and row 0 of the tensor grid.

### -field point21

The coordinate-space location of the control point in column 2 and row 1 of the tensor grid.

### -field point22

The coordinate-space location of the control point in column 2 and row 2 of the tensor grid.

### -field point23

The coordinate-space location of the control point in column 2 and row 3 of the tensor grid.

### -field point30

The coordinate-space location of the control point in column 3 and row 0 of the tensor grid.

### -field point31

The coordinate-space location of the control point in column 3 and row 1 of the tensor grid.

### -field point32

The coordinate-space location of the control point in column 3 and row 2 of the tensor grid.

### -field point33

The coordinate-space location of the control point in column 3 and row 3 of the tensor grid.

### -field color00

The color associated with the control point in column 0 and row 0 of the tensor grid.

### -field color03

The color associated with the control point in column 0 and row 3 of the tensor grid.

### -field color30

The color associated with the control point in column 3 and row 0 of the tensor grid.

### -field color33

The color associated with the control point in column 3 and row 3 of the tensor grid.

### -field topEdgeMode

Specifies how to render the top edge of the mesh.

### -field leftEdgeMode

Specifies how to render the left edge of the mesh.

### -field bottomEdgeMode

Specifies how to render the bottom edge of the mesh.

### -field rightEdgeMode

Specifies how to render the right edge of the mesh.

## -remarks

The following image shows the numbering of control points on a tensor grid.

<img alt="Number of control points on a tensor grid" src="./images/tensorpatch.png"/>