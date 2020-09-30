---
UID: NS:d3d11.D3D11_TEX2DMS_ARRAY_RTV
title: D3D11_TEX2DMS_ARRAY_RTV (d3d11.h)
description: Specifies the subresources from a an array of multisampled 2D textures to use in a render-target view.
helpviewer_keywords: ["D3D11_TEX2DMS_ARRAY_RTV","D3D11_TEX2DMS_ARRAY_RTV structure [Direct3D 11]","d3d11/D3D11_TEX2DMS_ARRAY_RTV","dd9c5839-fcab-1f5f-a4fe-866cc00f6bd2","direct3d11.d3d11_tex2dms_array_rtv"]
old-location: direct3d11\d3d11_tex2dms_array_rtv.htm
tech.root: direct3d11
ms.assetid: ec08341c-980f-4d5f-8eb9-f41835105b46
ms.date: 12/05/2018
ms.keywords: D3D11_TEX2DMS_ARRAY_RTV, D3D11_TEX2DMS_ARRAY_RTV structure [Direct3D 11], d3d11/D3D11_TEX2DMS_ARRAY_RTV, dd9c5839-fcab-1f5f-a4fe-866cc00f6bd2, direct3d11.d3d11_tex2dms_array_rtv
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
req.typenames: D3D11_TEX2DMS_ARRAY_RTV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX2DMS_ARRAY_RTV
 - d3d11/D3D11_TEX2DMS_ARRAY_RTV
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
 - D3D11_TEX2DMS_ARRAY_RTV
---

# D3D11_TEX2DMS_ARRAY_RTV structure


## -description

Specifies the subresources from a an array of multisampled 2D textures to use in a render-target view.

## -struct-fields

### -field FirstArraySlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the first texture to use in an array of textures.

### -field ArraySize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of textures to use.

## -remarks

This structure is one member of a render-target-view description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_render_target_view_desc">D3D11_RENDER_TARGET_VIEW_DESC</a>).

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>