---
UID: NE:d3d12.D3D12_VIEW_INSTANCING_TIER
title: D3D12_VIEW_INSTANCING_TIER (d3d12.h)
description: Indicates the tier level at which view instancing is supported.
helpviewer_keywords: ["D3D12_VIEW_INSTANCING_TIER","D3D12_VIEW_INSTANCING_TIER enumeration","D3D12_VIEW_INSTANCING_TIER_1","D3D12_VIEW_INSTANCING_TIER_2","D3D12_VIEW_INSTANCING_TIER_3","D3D12_VIEW_INSTANCING_TIER_NOT_SUPPORTED","d3d12/D3D12_VIEW_INSTANCING_TIER","d3d12/D3D12_VIEW_INSTANCING_TIER_1","d3d12/D3D12_VIEW_INSTANCING_TIER_2","d3d12/D3D12_VIEW_INSTANCING_TIER_3","d3d12/D3D12_VIEW_INSTANCING_TIER_NOT_SUPPORTED","direct3d12.d3d12_view_instancing_tier"]
old-location: direct3d12\d3d12_view_instancing_tier.htm
tech.root: direct3d12
ms.assetid: BB89E374-0447-40BE-AF89-D07BFCCF93FA
ms.date: 12/05/2018
ms.keywords: D3D12_VIEW_INSTANCING_TIER, D3D12_VIEW_INSTANCING_TIER enumeration, D3D12_VIEW_INSTANCING_TIER_1, D3D12_VIEW_INSTANCING_TIER_2, D3D12_VIEW_INSTANCING_TIER_3, D3D12_VIEW_INSTANCING_TIER_NOT_SUPPORTED, d3d12/D3D12_VIEW_INSTANCING_TIER, d3d12/D3D12_VIEW_INSTANCING_TIER_1, d3d12/D3D12_VIEW_INSTANCING_TIER_2, d3d12/D3D12_VIEW_INSTANCING_TIER_3, d3d12/D3D12_VIEW_INSTANCING_TIER_NOT_SUPPORTED, direct3d12.d3d12_view_instancing_tier
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
req.typenames: D3D12_VIEW_INSTANCING_TIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_VIEW_INSTANCING_TIER
 - d3d12/D3D12_VIEW_INSTANCING_TIER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_VIEW_INSTANCING_TIER
---

# D3D12_VIEW_INSTANCING_TIER enumeration


## -description

Indicates the tier level at which view instancing is supported.

## -enum-fields

### -field D3D12_VIEW_INSTANCING_TIER_NOT_SUPPORTED:0

View instancing is not supported.

### -field D3D12_VIEW_INSTANCING_TIER_1:1

View instancing is supported by draw-call level looping only.

### -field D3D12_VIEW_INSTANCING_TIER_2:2

View instancing is supported by draw-call level looping at worst, but the GPU can perform view instancing more efficiently in certain circumstances which are architecture-dependent.

### -field D3D12_VIEW_INSTANCING_TIER_3:3

View instancing is supported and instancing begins with the first shader stage that references SV_ViewID or with rasterization if no shader stage references SV_ViewID. This means that redundant work is eliminated across view instances when it's not dependent on SV_ViewID. Before rasterization, work that doesn't directly depend on SV_ViewID is shared across all views; only work that depends on SV_ViewID is repeated for each view.

<div class="alert"><b>Note</b>  If a hull shader produces tessellation factors that are dependent on SV_ViewID, then tessellation and all subsequent work must be repeated per-view. Similarly, if the amount of geometry produced by the geometry shader depends on SV_ViewID, then the geometry shader must be repeated per-view before proceeding to rasterization.</div>
<div> </div>
View instance masking only effects whether work that directly depends on SV_ViewID is performed, not the entire loop iteration (per-view). If the view instance mask is non-0, some work that depends on SV_ViewID might still be performed on masked-off pixels but will have no externally-visible effect; for example, no UAV writes are performed and clipping/rasterization is not invoked. If the view instance mask is 0 no work is performed, including work that's not dependent on SV_ViewID.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
