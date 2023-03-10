---
UID: NS:d3d12.D3D12_VIEW_INSTANCE_LOCATION
title: D3D12_VIEW_INSTANCE_LOCATION (d3d12.h)
description: Specifies the viewport/stencil and render target associated with a view instance.
helpviewer_keywords: ["D3D12_VIEW_INSTANCE_LOCATION","D3D12_VIEW_INSTANCE_LOCATION structure","d3d12/D3D12_VIEW_INSTANCE_LOCATION","direct3d12.d3d12_view_instance_location"]
old-location: direct3d12\d3d12_view_instance_location.htm
tech.root: direct3d12
ms.assetid: 10E5956E-6DFB-447D-8D1A-C1A41A1C4A03
ms.date: 12/05/2018
ms.keywords: D3D12_VIEW_INSTANCE_LOCATION, D3D12_VIEW_INSTANCE_LOCATION structure, d3d12/D3D12_VIEW_INSTANCE_LOCATION, direct3d12.d3d12_view_instance_location
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
req.typenames: D3D12_VIEW_INSTANCE_LOCATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_VIEW_INSTANCE_LOCATION
 - d3d12/D3D12_VIEW_INSTANCE_LOCATION
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
 - D3D12_VIEW_INSTANCE_LOCATION
---

# D3D12_VIEW_INSTANCE_LOCATION structure


## -description

Specifies the viewport/stencil and render target associated with a view instance.

## -struct-fields

### -field ViewportArrayIndex

The index of the viewport in the viewports array to be used by the view instance associated with this location.

### -field RenderTargetArrayIndex

The index of the render target in the render targets array to be used by the view instance associated with this location.

## -remarks

The values specified in a view instance location structure can be added to ViewportArrayIndex and RenderTargetArrayIndex values output by the shader prior to rasterization to compute the final effective index of the viewport and render target to send primitives to. If a computed index is out of range (that is, when the index is larger than the number of viewport or render target elements in their respective arrays) then the effective index becomes 0.

For shaders that dynamically select the viewport or render target indices, an application can set all the view instance locations declared in a PSO to the same value to act as a uniform base value for all views.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>