---
UID: NF:d3d12.ID3D12GraphicsCommandList5.RSSetShadingRate
title: ID3D12GraphicsCommandList5::RSSetShadingRate
ms.date: 01/31/19
ms.keywords: ID3D12GraphicsCommandList5::RSSetShadingRate
ms.topic: language-reference
f1_keywords: 
 - "d3d12/ID3D12GraphicsCommandList5::RSSetShadingRate"
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: d3d12.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.h
api_name:
 - ID3D12GraphicsCommandList5::RSSetShadingRate
---

## -description

Sets the base shading rate, and combiners, for variable-rate shading (VRS). For more info, see [Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs).

## -parameters

### -param baseShadingRate

Type: [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)

A constant from the [D3D12_SHADING_RATE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) enumeration describing the base shading rate to set.

### -param combiners

Type: **const [D3D12_SHADING_RATE_COMBINER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner)\***

An optional pointer to a constant array of [D3D12_SHADING_RATE_COMBINER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner) containing the shading rate combiners to set. The count of **D3D12_SHADING_RATE_COMBINER** elements in the array must be equal to the constant [D3D12_RS_SET_SHADING_RATE_COMBINER_COUNT](/windows/desktop/direct3d12/constants).

## -remarks

## -see-also

[Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs)
