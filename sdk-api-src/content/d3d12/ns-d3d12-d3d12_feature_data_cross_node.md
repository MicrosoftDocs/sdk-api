---
UID: NS:d3d12.D3D12_FEATURE_DATA_CROSS_NODE
title: D3D12_FEATURE_DATA_CROSS_NODE
description: Indicates the level of support for the sharing of resources between different adapters&mdash;for example, multiple GPUs.
tech.root: direct3d12
helpviewer_keywords: ["D3D12_FEATURE_DATA_CROSS_NODE"]
ms.date: 05/20/2019
ms.keywords: D3D12_FEATURE_DATA_CROSS_NODE
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_CROSS_NODE
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_FEATURE_DATA_CROSS_NODE
 - d3d12/D3D12_FEATURE_DATA_CROSS_NODE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_CROSS_NODE
---

## -description

Indicates the level of support for the sharing of resources between different adapters&mdash;for example, multiple GPUs.

## -struct-fields

### -field SharingTier

Type: <b>[D3D12_CROSS_NODE_SHARING_TIER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier)</b>

Indicates the tier of cross-adapter sharing support.

### -field AtomicShaderInstructions

Type: <b>[BOOL](/windows/desktop/winprog/windows-data-types)</b>

Indicates there is support for shader instructions which operate across adapters.

## -remarks

## -see-also

