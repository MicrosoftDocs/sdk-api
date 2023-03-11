---
UID: NE:d3d11.D3D11_FILTER_REDUCTION_TYPE
title: D3D11_FILTER_REDUCTION_TYPE (d3d11.h)
description: Specifies the type of sampler filter reduction.
helpviewer_keywords: ["D3D11_FILTER_REDUCTION_TYPE","D3D11_FILTER_REDUCTION_TYPE enumeration [Direct3D 11]","D3D11_FILTER_REDUCTION_TYPE_COMPARISON","D3D11_FILTER_REDUCTION_TYPE_MAXIMUM","D3D11_FILTER_REDUCTION_TYPE_MINIMUM","D3D11_FILTER_REDUCTION_TYPE_STANDARD","d3d11/D3D11_FILTER_REDUCTION_TYPE","d3d11/D3D11_FILTER_REDUCTION_TYPE_COMPARISON","d3d11/D3D11_FILTER_REDUCTION_TYPE_MAXIMUM","d3d11/D3D11_FILTER_REDUCTION_TYPE_MINIMUM","d3d11/D3D11_FILTER_REDUCTION_TYPE_STANDARD","direct3d11.d3d11_filter_reduction_type"]
old-location: direct3d11\d3d11_filter_reduction_type.htm
tech.root: direct3d11
ms.assetid: 9124D1DE-8045-49DA-83A6-634083C79C84
ms.date: 12/05/2018
ms.keywords: D3D11_FILTER_REDUCTION_TYPE, D3D11_FILTER_REDUCTION_TYPE enumeration [Direct3D 11], D3D11_FILTER_REDUCTION_TYPE_COMPARISON, D3D11_FILTER_REDUCTION_TYPE_MAXIMUM, D3D11_FILTER_REDUCTION_TYPE_MINIMUM, D3D11_FILTER_REDUCTION_TYPE_STANDARD, d3d11/D3D11_FILTER_REDUCTION_TYPE, d3d11/D3D11_FILTER_REDUCTION_TYPE_COMPARISON, d3d11/D3D11_FILTER_REDUCTION_TYPE_MAXIMUM, d3d11/D3D11_FILTER_REDUCTION_TYPE_MINIMUM, d3d11/D3D11_FILTER_REDUCTION_TYPE_STANDARD, direct3d11.d3d11_filter_reduction_type
req.header: d3d11.h
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
req.typenames: D3D11_FILTER_REDUCTION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FILTER_REDUCTION_TYPE
 - d3d11/D3D11_FILTER_REDUCTION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_FILTER_REDUCTION_TYPE
---

# D3D11_FILTER_REDUCTION_TYPE enumeration


## -description

Specifies the type of sampler filter reduction.

## -enum-fields

### -field D3D11_FILTER_REDUCTION_TYPE_STANDARD:0

Indicates standard (default) filter reduction.

### -field D3D11_FILTER_REDUCTION_TYPE_COMPARISON:1

Indicates a comparison filter reduction.

### -field D3D11_FILTER_REDUCTION_TYPE_MINIMUM:2

Indicates minimum filter reduction.

### -field D3D11_FILTER_REDUCTION_TYPE_MAXIMUM:3

Indicates maximum filter reduction.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc">D3D11_SAMPLER_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
