---
UID: NS:d3d12.D3D12_HIT_GROUP_DESC
title: D3D12_HIT_GROUP_DESC (d3d12.h)
description: Describes a raytracing hit group state subobject that can be included in a state object.
helpviewer_keywords: ["D3D12_HIT_GROUP_DESC","D3D12_HIT_GROUP_DESC structure","PD3D12_HIT_GROUP_DESC","PD3D12_HIT_GROUP_DESC structure pointer","d3d12/D3D12_HIT_GROUP_DESC","d3d12/PD3D12_HIT_GROUP_DESC","direct3d12.d3d12_hit_group_desc"]
old-location: direct3d12\d3d12_hit_group_desc.htm
tech.root: direct3d12
ms.assetid: 6ADE3175-F133-4C45-8D53-E6A3220B00B0
ms.date: 12/05/2018
ms.keywords: D3D12_HIT_GROUP_DESC, D3D12_HIT_GROUP_DESC structure, PD3D12_HIT_GROUP_DESC, PD3D12_HIT_GROUP_DESC structure pointer, d3d12/D3D12_HIT_GROUP_DESC, d3d12/PD3D12_HIT_GROUP_DESC, direct3d12.d3d12_hit_group_desc
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
req.typenames: D3D12_HIT_GROUP_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_HIT_GROUP_DESC
 - d3d12/D3D12_HIT_GROUP_DESC
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
 - D3D12_HIT_GROUP_DESC
---

# D3D12_HIT_GROUP_DESC structure


## -description

Describes a raytracing hit group state subobject that can be included in a state object.

## -struct-fields

### -field HitGroupExport

The name of the hit group.

### -field Type

A value from the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_hit_group_type">D3D12_HIT_GROUP_TYPE</a> enumeration specifying the type of the hit group.

### -field AnyHitShaderImport

Optional name of the any-hit shader associated with the hit group. This field can be used with all hit group types.

### -field ClosestHitShaderImport

Optional name of the closest-hit shader associated with the hit group. This field can be used with all hit group types.

### -field IntersectionShaderImport

Optional name of the intersection shader associated with the hit group.  This field can only be used with hit groups of type procedural primitive.