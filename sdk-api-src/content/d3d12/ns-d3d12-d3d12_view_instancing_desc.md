---
UID: NS:d3d12.D3D12_VIEW_INSTANCING_DESC
title: D3D12_VIEW_INSTANCING_DESC (d3d12.h)
description: Specifies parameters used during view instancing configuration.
helpviewer_keywords: ["D3D12_VIEW_INSTANCING_DESC","D3D12_VIEW_INSTANCING_DESC structure","d3d12/D3D12_VIEW_INSTANCING_DESC","direct3d12.d3d12_view_instancing_desc"]
old-location: direct3d12\d3d12_view_instancing_desc.htm
tech.root: direct3d12
ms.assetid: AFB7AB23-9A59-49D7-8C3E-222C3AED2314
ms.date: 12/05/2018
ms.keywords: D3D12_VIEW_INSTANCING_DESC, D3D12_VIEW_INSTANCING_DESC structure, d3d12/D3D12_VIEW_INSTANCING_DESC, direct3d12.d3d12_view_instancing_desc
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
req.typenames: D3D12_VIEW_INSTANCING_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_VIEW_INSTANCING_DESC
 - d3d12/D3D12_VIEW_INSTANCING_DESC
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
 - D3D12_VIEW_INSTANCING_DESC
---

# D3D12_VIEW_INSTANCING_DESC structure


## -description

Specifies parameters used during view instancing configuration.

## -struct-fields

### -field ViewInstanceCount

Specifies the number of views to be used, up to D3D12_MAX_VIEW_INSTANCE_COUNT.

### -field pViewInstanceLocations

The address of a memory location that contains <b>ViewInstanceCount</b> view instance location structures that specify the location of viewport/scissor and render target details of each view instance.

### -field Flags

Configures view instancing with additional options.

## -remarks

View instancing is declared in a PSO using this structure. The view instance count is set in the PSO to allow whole-pipeline optimization based on the number of views.

View instancing is disabled when it's not declared in the PSO or when ViewInstanceCount is set to 0. When disabled, rendering behaves as if view instancing is enabled and ViewInstanceCount is set to 1; shaders only see a value of 0 in SV_ViewID and just one view instance is produced. This allows shaders that are aware of view instancing to still be used in PSOs that disable it. Some adapters might support shader model 6.1 (which exposes SV_ViewID) but not view instancing; these adapters must still support shaders that input SV_ViewID in PSOs that declare ViewInstanceCount as 0 or 1.

The shader prior to rasterization can output SV_RenderTargetArrayIndex and SV_ViewportArrayIndex values which don't have to depend on SV_ViewID. To compute the final effective index of the viewport and render target where primitives will be sent, these values, when present, are added to the ViewportArrayIndex and RenderTargetArrayIndex values of the view instance locations declared in the PSO. If a computed index is out of range (that is, when the index is larger than the number of viewport or render target elements in their respective arrays) then the effective index becomes 0.

For shaders that dynamically select the viewport or render target indices, an application can set all the view instance locations declared in the PSO to a single value (such as 0) to act as a uniform base index to which the dynamically-selected SV_RenderTargetArrayIndex and SV_ViewportArrayIndex values are added.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>