---
UID: NS:d3d12.D3D12_TEX2DMS_DSV
title: D3D12_TEX2DMS_DSV (d3d12.h)
description: Describes the subresource from a multi sampled 2D texture that is accessible to a depth-stencil view.
helpviewer_keywords: ["D3D12_TEX2DMS_DSV","D3D12_TEX2DMS_DSV structure","d3d12/D3D12_TEX2DMS_DSV","direct3d12.d3d12_tex2dms_dsv"]
old-location: direct3d12\d3d12_tex2dms_dsv.htm
tech.root: direct3d12
ms.assetid: 3FECACFB-6635-4AA3-A568-57A3CE8754AF
ms.date: 12/05/2018
ms.keywords: D3D12_TEX2DMS_DSV, D3D12_TEX2DMS_DSV structure, d3d12/D3D12_TEX2DMS_DSV, direct3d12.d3d12_tex2dms_dsv
req.header: d3d12.h
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
req.typenames: D3D12_TEX2DMS_DSV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TEX2DMS_DSV
 - d3d12/D3D12_TEX2DMS_DSV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_TEX2DMS_DSV
---

# D3D12_TEX2DMS_DSV structure


## -description

Describes the subresource from a multi sampled 2D texture that is accessible to a depth-stencil view.

## -struct-fields

### -field UnusedField_NothingToDefine

Unused.

## -remarks

This structure is a member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc">D3D12_DEPTH_STENCIL_VIEW_DESC</a> structure.

Because a multi sampled 2D texture contains a single subresource, there is nothing to specify in <b>D3D12_TEX2DMS_DSV</b>. Consequently, <b>UnusedField_NothingToDefine</b> is included so that this structure will compile in C.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>