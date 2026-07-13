---
UID: NS:d3d12.D3D12_TEX2D_UAV
title: D3D12_TEX2D_UAV (d3d12.h)
description: Describes a unordered-access 2D texture resource. (D3D12_TEX2D_UAV)
helpviewer_keywords: ["D3D12_TEX2D_UAV","D3D12_TEX2D_UAV structure","d3d12/D3D12_TEX2D_UAV","direct3d12.d3d12_tex2d_uav"]
old-location: direct3d12\d3d12_tex2d_uav.htm
tech.root: direct3d12
ms.assetid: 4AC4B783-DF03-4BBF-A1F3-F21E1D9820D2
ms.date: 12/05/2018
ms.keywords: D3D12_TEX2D_UAV, D3D12_TEX2D_UAV structure, d3d12/D3D12_TEX2D_UAV, direct3d12.d3d12_tex2d_uav
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
req.typenames: D3D12_TEX2D_UAV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TEX2D_UAV
 - d3d12/D3D12_TEX2D_UAV
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
 - D3D12_TEX2D_UAV
---

# D3D12_TEX2D_UAV structure


## -description

Describes a unordered-access 2D texture resource.

## -struct-fields

### -field MipSlice

The mipmap slice index.

### -field PlaneSlice

The index (plane slice number) of the plane to use in the texture.

## -remarks

Use this structure with a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc">D3D12_UNORDERED_ACCESS_VIEW_DESC</a> structure to view the resource as a 2D texture.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
