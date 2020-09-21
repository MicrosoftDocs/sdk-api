---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS3
title: D3D12_FEATURE_DATA_D3D12_OPTIONS3 (d3d12.h)
description: Indicates the level of support that the adapter provides for timestamp queries, format-casting, immediate write, view instancing, and barycentrics.
helpviewer_keywords: ["D3D12_FEATURE_DATA_D3D12_OPTIONS3","D3D12_FEATURE_DATA_D3D12_OPTIONS3 structure","d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS3","direct3d12.d3d12_feature_data_d3d12_options3"]
old-location: direct3d12\d3d12_feature_data_d3d12_options3.htm
tech.root: direct3d12
ms.assetid: 4BA37E6A-124D-4808-8005-CC049B8EE165
ms.date: 12/05/2018
ms.keywords: D3D12_FEATURE_DATA_D3D12_OPTIONS3, D3D12_FEATURE_DATA_D3D12_OPTIONS3 structure, d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS3, direct3d12.d3d12_feature_data_d3d12_options3
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
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS3
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS3
 - d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS3
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
 - D3D12_FEATURE_DATA_D3D12_OPTIONS3
---

# D3D12_FEATURE_DATA_D3D12_OPTIONS3 structure


## -description

Indicates the level of support that the adapter provides for timestamp queries, format-casting, immediate write, view instancing, and barycentrics.

## -struct-fields

### -field CopyQueueTimestampQueriesSupported

Indicates whether timestamp queries are supported on copy queues.

### -field CastingFullyTypedFormatSupported

Indicates whether casting from one fully typed format to another, compatible, format is supported.

### -field WriteBufferImmediateSupportFlags

Indicates the kinds of command lists that support the ability to write an immediate value directly from the command stream into a specified buffer.

### -field ViewInstancingTier

Indicates the level of support the adapter has for view instancing.

### -field BarycentricsSupported

Indicates whether barycentrics are supported.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>