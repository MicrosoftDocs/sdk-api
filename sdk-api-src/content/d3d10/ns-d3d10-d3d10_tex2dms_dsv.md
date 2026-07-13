---
UID: NS:d3d10.D3D10_TEX2DMS_DSV
title: D3D10_TEX2DMS_DSV (d3d10.h)
description: Specifies the subresource from a multisampled 2D texture that is accessible to a depth-stencil view. (D3D10_TEX2DMS_DSV)
helpviewer_keywords: ["D3D10_TEX2DMS_DSV","D3D10_TEX2DMS_DSV structure [Direct3D 10]","c5f5656b-8589-3a09-033c-cf23c7b8dea4","d3d10/D3D10_TEX2DMS_DSV","direct3d10.d3d10_tex2dms_dsv"]
old-location: direct3d10\d3d10_tex2dms_dsv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex2dms_dsv.htm
ms.date: 12/05/2018
ms.keywords: D3D10_TEX2DMS_DSV, D3D10_TEX2DMS_DSV structure [Direct3D 10], c5f5656b-8589-3a09-033c-cf23c7b8dea4, d3d10/D3D10_TEX2DMS_DSV, direct3d10.d3d10_tex2dms_dsv
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
req.typenames: D3D10_TEX2DMS_DSV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_TEX2DMS_DSV
 - d3d10/D3D10_TEX2DMS_DSV
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
 - D3D10_TEX2DMS_DSV
---

# D3D10_TEX2DMS_DSV structure


## -description

Specifies the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource</a> from a multisampled <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">2D texture</a> that is accessible to a depth-stencil view.

## -struct-fields

### -field UnusedField_NothingToDefine

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Unused.

## -remarks

Since a multisampled 2D texture contains a single subtexture, there is nothing to specify; this unused member is included so that this structure will compile in C.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>
