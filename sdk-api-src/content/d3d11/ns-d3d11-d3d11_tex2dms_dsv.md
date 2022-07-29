---
UID: NS:d3d11.D3D11_TEX2DMS_DSV
title: D3D11_TEX2DMS_DSV (d3d11.h)
description: Specifies the subresource from a multisampled 2D texture that is accessible to a depth-stencil view. (D3D11_TEX2DMS_DSV)
helpviewer_keywords: ["8d27f5d8-2d28-1d90-094b-7cb4d66f7887","D3D11_TEX2DMS_DSV","D3D11_TEX2DMS_DSV structure [Direct3D 11]","d3d11/D3D11_TEX2DMS_DSV","direct3d11.d3d11_tex2dms_dsv"]
old-location: direct3d11\d3d11_tex2dms_dsv.htm
tech.root: direct3d11
ms.assetid: 1723044b-1942-4373-8040-0c47b680ea95
ms.date: 12/05/2018
ms.keywords: 8d27f5d8-2d28-1d90-094b-7cb4d66f7887, D3D11_TEX2DMS_DSV, D3D11_TEX2DMS_DSV structure [Direct3D 11], d3d11/D3D11_TEX2DMS_DSV, direct3d11.d3d11_tex2dms_dsv
req.header: d3d11.h
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
req.typenames: D3D11_TEX2DMS_DSV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX2DMS_DSV
 - d3d11/D3D11_TEX2DMS_DSV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_TEX2DMS_DSV
---

# D3D11_TEX2DMS_DSV structure


## -description

Specifies the subresource from a multisampled 2D texture that is accessible to a depth-stencil view.

## -struct-fields

### -field UnusedField_NothingToDefine

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Unused.

## -remarks

Because a multisampled 2D texture contains a single subtexture, there is nothing to specify; this unused member is included so that this structure will compile in C.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
