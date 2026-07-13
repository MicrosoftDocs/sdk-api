---
UID: NS:d3d12.D3D12_FEATURE_DATA_SERIALIZATION
title: D3D12_FEATURE_DATA_SERIALIZATION
description: Indicates the level of support for heap serialization.
helpviewer_keywords: ["D3D12_FEATURE_DATA_SERIALIZATION"]
tech.root: direct3d12
ms.date: 05/20/2019
ms.keywords: D3D12_FEATURE_DATA_SERIALIZATION
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
req.typenames: D3D12_FEATURE_DATA_SERIALIZATION
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_FEATURE_DATA_SERIALIZATION
 - d3d12/D3D12_FEATURE_DATA_SERIALIZATION
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_SERIALIZATION
---

## -description

Indicates the level of support for heap serialization.

## -struct-fields

### -field NodeIndex

Type: **[UINT](/windows/desktop/WinProg/windows-data-types)**

An input field, indicating the adapter index to query.

### -field HeapSerializationTier

Type: **[D3D12_HEAP_SERIALIZATION_TIER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_serialization_tier)**

An output field, indicating the tier of heap serialization support.

## -remarks

## -see-also

