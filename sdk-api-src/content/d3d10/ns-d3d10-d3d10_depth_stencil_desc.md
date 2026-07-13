---
UID: NS:d3d10.D3D10_DEPTH_STENCIL_DESC
title: D3D10_DEPTH_STENCIL_DESC (d3d10.h)
description: Describes depth-stencil state. (D3D10_DEPTH_STENCIL_DESC)
helpviewer_keywords: ["D3D10_DEPTH_STENCIL_DESC","D3D10_DEPTH_STENCIL_DESC structure [Direct3D 10]","bc44a5f2-b12b-88c0-0985-df3e7b45b998","d3d10/D3D10_DEPTH_STENCIL_DESC","direct3d10.d3d10_depth_stencil_desc"]
old-location: direct3d10\d3d10_depth_stencil_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_depth_stencil_desc.htm
ms.date: 12/05/2018
ms.keywords: D3D10_DEPTH_STENCIL_DESC, D3D10_DEPTH_STENCIL_DESC structure [Direct3D 10], bc44a5f2-b12b-88c0-0985-df3e7b45b998, d3d10/D3D10_DEPTH_STENCIL_DESC, direct3d10.d3d10_depth_stencil_desc
req.header: d3d10.h
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
req.typenames: D3D10_DEPTH_STENCIL_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_DEPTH_STENCIL_DESC
 - d3d10/D3D10_DEPTH_STENCIL_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_DEPTH_STENCIL_DESC
---

# D3D10_DEPTH_STENCIL_DESC structure


## -description

Describes depth-stencil state.

## -struct-fields

### -field DepthEnable

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

A Boolean value that enables depth testing.  The default value is <b>TRUE</b>.

### -field DepthWriteMask

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_depth_write_mask">D3D10_DEPTH_WRITE_MASK</a></b>

A member of the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_depth_write_mask">D3D10_DEPTH_WRITE_MASK</a> enumerated type that identifies a portion of the depth-stencil buffer that can be modified by depth data.  The default value is <b>D3D10_DEPTH_WRITE_MASK_ALL</b>.

### -field DepthFunc

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_comparison_func">D3D10_COMPARISON_FUNC</a></b>

A member of the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_comparison_func">D3D10_COMPARISON_FUNC</a> enumerated type that defines how depth data is compared against existing depth data.  The default value is <b>D3D10_COMPARISON_LESS</b>

### -field StencilEnable

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

A Boolean value that enables stencil testing.  The default value is <b>FALSE</b>.

### -field StencilReadMask

Type: <b>UINT8</b>

A value that identifies a portion of the depth-stencil buffer for reading stencil data.  The default value is <b>D3D10_DEFAULT_STENCIL_READ_MASK</b>.

### -field StencilWriteMask

Type: <b>UINT8</b>

A value that identifies a portion of the depth-stencil buffer for writing stencil data. The default value is <b>D3D10_DEFAULT_STENCIL_WRITE_MASK</b>.

### -field FrontFace

Type: <b><a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_depth_stencilop_desc">D3D10_DEPTH_STENCILOP_DESC</a></b>

A <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_depth_stencilop_desc">D3D10_DEPTH_STENCILOP_DESC</a> structure that identifies how to use the results of the depth test and the stencil test for pixels whose surface normal is facing toward the camera.

### -field BackFace

Type: <b><a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_depth_stencilop_desc">D3D10_DEPTH_STENCILOP_DESC</a></b>

A <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_depth_stencilop_desc">D3D10_DEPTH_STENCILOP_DESC</a> structure that identifies how to use the results of the depth test and the stencil test for pixels whose surface normal is facing away from the camera.

## -remarks

Depth-stencil state controls how <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">depth-stencil</a> testing is performed by the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger</a> stage.

The formats that support stenciling are DXGI_FORMAT_D24_UNORM_S8_UINT and DXGI_FORMAT_D32_FLOAT_S8X24_UINT.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>
