---
UID: NE:d3d12.D3D12_FILTER_REDUCTION_TYPE
title: D3D12_FILTER_REDUCTION_TYPE (d3d12.h)
description: Specifies the type of filter reduction.
helpviewer_keywords: ["D3D12_FILTER_REDUCTION_TYPE","D3D12_FILTER_REDUCTION_TYPE enumeration","D3D12_FILTER_REDUCTION_TYPE_COMPARISON","D3D12_FILTER_REDUCTION_TYPE_MAXIMUM","D3D12_FILTER_REDUCTION_TYPE_MINIMUM","D3D12_FILTER_REDUCTION_TYPE_STANDARD","d3d12/D3D12_FILTER_REDUCTION_TYPE","d3d12/D3D12_FILTER_REDUCTION_TYPE_COMPARISON","d3d12/D3D12_FILTER_REDUCTION_TYPE_MAXIMUM","d3d12/D3D12_FILTER_REDUCTION_TYPE_MINIMUM","d3d12/D3D12_FILTER_REDUCTION_TYPE_STANDARD","direct3d12.d3d12_filter_reduction_type"]
old-location: direct3d12\d3d12_filter_reduction_type.htm
tech.root: direct3d12
ms.assetid: C180B6BD-A73C-4D21-9AC0-F9D4FCC2B4E7
ms.date: 12/05/2018
ms.keywords: D3D12_FILTER_REDUCTION_TYPE, D3D12_FILTER_REDUCTION_TYPE enumeration, D3D12_FILTER_REDUCTION_TYPE_COMPARISON, D3D12_FILTER_REDUCTION_TYPE_MAXIMUM, D3D12_FILTER_REDUCTION_TYPE_MINIMUM, D3D12_FILTER_REDUCTION_TYPE_STANDARD, d3d12/D3D12_FILTER_REDUCTION_TYPE, d3d12/D3D12_FILTER_REDUCTION_TYPE_COMPARISON, d3d12/D3D12_FILTER_REDUCTION_TYPE_MAXIMUM, d3d12/D3D12_FILTER_REDUCTION_TYPE_MINIMUM, d3d12/D3D12_FILTER_REDUCTION_TYPE_STANDARD, direct3d12.d3d12_filter_reduction_type
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
req.typenames: D3D12_FILTER_REDUCTION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FILTER_REDUCTION_TYPE
 - d3d12/D3D12_FILTER_REDUCTION_TYPE
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
 - D3D12_FILTER_REDUCTION_TYPE
---

# D3D12_FILTER_REDUCTION_TYPE enumeration


## -description

Specifies the type of filter reduction.

## -enum-fields

### -field D3D12_FILTER_REDUCTION_TYPE_STANDARD:0

The filter type is standard.

### -field D3D12_FILTER_REDUCTION_TYPE_COMPARISON:1

The filter type is comparison.

### -field D3D12_FILTER_REDUCTION_TYPE_MINIMUM:2

The filter type is minimum.

### -field D3D12_FILTER_REDUCTION_TYPE_MAXIMUM:3

The filter type is maximum.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc">D3D12_SAMPLER_DESC</a> structure. Also, refer to the remarks for <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter">D3D12_FILTER</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
