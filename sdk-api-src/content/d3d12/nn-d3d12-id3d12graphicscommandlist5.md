---
UID: NN:d3d12.ID3D12GraphicsCommandList5
title: ID3D12GraphicsCommandList5
description: Encapsulates a list of graphics commands for rendering, extending the interface to support variable-rate shading (VRS).
helpviewer_keywords: ["ID3D12GraphicsCommandList5"]
tech.root: direct3d12
ms.date: 05/20/2019
ms.keywords: ID3D12GraphicsCommandList5
f1_keywords:
- d3d12/ID3D12GraphicsCommandList5
dev_langs:
- c++
targetos: Windows
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: d3d12.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
- apiref
api_type:
- COM
api_location:
- d3d12.h
api_name:
- ID3D12GraphicsCommandList5
---

## -description

Encapsulates a list of graphics commands for rendering, extending the interface to support variable-rate shading (VRS). For more info, see [Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs).

## Inheritance

The **ID3D12GraphicsCommandList5** interface inherits from the [ID3D12GraphicsCommandList4](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist4) interface.

## -members

The **ID3D12GraphicsCommandList5** interface has these methods.

|Method|Description|
|-|-|
|[RSSetShadingRate](nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate.md)|Sets the base shading rate, and combiners, for variable-rate shading (VRS).|
|[RSSetShadingRateImage](nf-d3d12-id3d12graphicscommandlist5-rssetshadingrateimage.md)|Sets the screen-space shading-rate image for variable-rate shading (VRS).|

## -remarks

## -see-also

[Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs)
