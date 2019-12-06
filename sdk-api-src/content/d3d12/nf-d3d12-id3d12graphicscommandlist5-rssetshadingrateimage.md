---
UID: NF:d3d12.ID3D12GraphicsCommandList5.RSSetShadingRateImage
title: ID3D12GraphicsCommandList5::RSSetShadingRateImage
tech.root: direct3d12
ms.date: 01/31/19
ms.keywords: ID3D12GraphicsCommandList5::RSSetShadingRateImage
ms.topic: language-reference
f1_keywords:
- d3d12/ID3D12GraphicsCommandList5::RSSetShadingRateImage
dev_langs:
- c++
targetos: Windows
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
- ID3D12GraphicsCommandList5::RSSetShadingRateImage
---

## -description

Sets the screen-space shading-rate image for variable-rate shading (VRS). For more info, see [Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs).

## -parameters

### -param shadingRateImage

Type: **[ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

An optional pointer to an [ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) representing a screen-space shading-rate image.

## -remarks

## -see-also

[Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs)
