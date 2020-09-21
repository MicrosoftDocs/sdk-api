---
UID: NS:d3d12.D3D12_TEX2DMS_RTV
title: D3D12_TEX2DMS_RTV (d3d12.h)
description: Describes the subresource from a multi sampled 2D texture to use in a render-target view.
helpviewer_keywords: ["D3D12_TEX2DMS_RTV","D3D12_TEX2DMS_RTV structure","d3d12/D3D12_TEX2DMS_RTV","direct3d12.d3d12_tex2dms_rtv"]
old-location: direct3d12\d3d12_tex2dms_rtv.htm
tech.root: direct3d12
ms.assetid: 000B37D4-261D-48E1-B7ED-EEA1EC2DA0DD
ms.date: 12/05/2018
ms.keywords: D3D12_TEX2DMS_RTV, D3D12_TEX2DMS_RTV structure, d3d12/D3D12_TEX2DMS_RTV, direct3d12.d3d12_tex2dms_rtv
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
req.typenames: D3D12_TEX2DMS_RTV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TEX2DMS_RTV
 - d3d12/D3D12_TEX2DMS_RTV
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
 - D3D12_TEX2DMS_RTV
---

# D3D12_TEX2DMS_RTV structure


## -description

Describes the subresource from a multi sampled 2D texture to use in a render-target view.

## -struct-fields

### -field UnusedField_NothingToDefine

Integer of any value. See remarks.

## -remarks

This structure is a member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc">D3D12_RENDER_TARGET_VIEW_DESC</a> structure.

Because a multi sampled 2D texture contains a single subresource, there is actually nothing to specify in <b>D3D12_TEX2DMS_RTV</b>. Consequently, <b>UnusedField_NothingToDefine</b> is included so that this structure will compile in C.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>