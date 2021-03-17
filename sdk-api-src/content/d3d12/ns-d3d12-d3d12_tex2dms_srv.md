---
UID: NS:d3d12.D3D12_TEX2DMS_SRV
title: D3D12_TEX2DMS_SRV (d3d12.h)
description: Describes the subresources from a multi sampled 2D texture to use in a shader-resource view.
helpviewer_keywords: ["D3D12_TEX2DMS_SRV","D3D12_TEX2DMS_SRV structure","d3d12/D3D12_TEX2DMS_SRV","direct3d12.d3d12_tex2dms_srv"]
old-location: direct3d12\d3d12_tex2dms_srv.htm
tech.root: direct3d12
ms.assetid: 65D0AC4E-E9D3-4D99-835C-AD9ED7528A1A
ms.date: 12/05/2018
ms.keywords: D3D12_TEX2DMS_SRV, D3D12_TEX2DMS_SRV structure, d3d12/D3D12_TEX2DMS_SRV, direct3d12.d3d12_tex2dms_srv
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
req.typenames: D3D12_TEX2DMS_SRV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TEX2DMS_SRV
 - d3d12/D3D12_TEX2DMS_SRV
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
 - D3D12_TEX2DMS_SRV
---

# D3D12_TEX2DMS_SRV structure


## -description

Describes the subresources from a multi sampled 2D texture to use in a shader-resource view.

## -struct-fields

### -field UnusedField_NothingToDefine

Integer of any value. See remarks.

## -remarks

This structure is a member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc">D3D12_SHADER_RESOURCE_VIEW_DESC</a> structure.

Since a multi sampled 2D texture contains a single subresource, there is actually nothing to specify in <b>D3D12_TEX2DMS_SRV</b>. Consequently, <b>UnusedField_NothingToDefine</b> is included so that this structure will compile in C.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>