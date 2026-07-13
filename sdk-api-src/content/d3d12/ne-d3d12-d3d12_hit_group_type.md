---
UID: NE:d3d12.D3D12_HIT_GROUP_TYPE
title: D3D12_HIT_GROUP_TYPE (d3d12.h)
description: Specifies the type of a raytracing hit group state subobject. Use a value from this enumeration with the D3D12_HIT_GROUP_DESC structure.
helpviewer_keywords: ["D3D12_HIT_GROUP_TYPE","D3D12_HIT_GROUP_TYPE enumeration","D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE","D3D12_HIT_GROUP_TYPE_TRIANGLES","d3d12/D3D12_HIT_GROUP_TYPE","d3d12/D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE","d3d12/D3D12_HIT_GROUP_TYPE_TRIANGLES","direct3d12.d3d12_hit_group_type"]
old-location: direct3d12\d3d12_hit_group_type.htm
tech.root: direct3d12
ms.assetid: F7C77720-CAAE-49E4-929B-E1A0BF9FFC1A
ms.date: 12/05/2018
ms.keywords: D3D12_HIT_GROUP_TYPE, D3D12_HIT_GROUP_TYPE enumeration, D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE, D3D12_HIT_GROUP_TYPE_TRIANGLES, d3d12/D3D12_HIT_GROUP_TYPE, d3d12/D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE, d3d12/D3D12_HIT_GROUP_TYPE_TRIANGLES, direct3d12.d3d12_hit_group_type
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
req.typenames: D3D12_HIT_GROUP_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_HIT_GROUP_TYPE
 - d3d12/D3D12_HIT_GROUP_TYPE
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
 - D3D12_HIT_GROUP_TYPE
---

# D3D12_HIT_GROUP_TYPE enumeration


## -description

Specifies the type of a raytracing hit group state subobject. Use a value from this enumeration with the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_hit_group_desc">D3D12_HIT_GROUP_DESC</a> structure.

## -enum-fields

### -field D3D12_HIT_GROUP_TYPE_TRIANGLES:0

The hit group uses a list of triangles to calculate ray hits. Hit groups that use triangles can’t contain an intersection shader.

### -field D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE:0x1

The hit group uses a procedural primitive within a bounding box to calculate ray hits. Hit groups that use procedural primitives must contain an intersection shader.
