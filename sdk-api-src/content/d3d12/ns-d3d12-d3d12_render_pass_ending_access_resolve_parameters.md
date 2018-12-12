---
UID: NS:d3d12.D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS
title: D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS
author: windows-sdk-content
description: Describes a resource to resolve to at the conclusion of a render pass.
old-location: direct3d12\d3d12_render_pass_ending_access_resolve_parameters.htm
tech.root: direct3d12
ms.assetid: AF081936-CF83-4FFF-BA81-83CEE6F85BFF
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS, D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS structure, d3d12/D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS, direct3d12.d3d12_render_pass_ending_access_resolve_parameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS
product: Windows
targetos: Windows
req.typenames: D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS
req.redist: 
---

# D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS structure


## -description


Describes a resource to resolve to at the conclusion of a render pass.


## -struct-fields




### -field pSrcResource

A pointer to an <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>. The source resource.


### -field pDstResource

A pointer to an <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>. The destination resource.


### -field SubresourceCount

A <b>UINT</b>. The number of subresources.


### -field pSubresourceParameters

A pointer to a constant array of <a href="https://msdn.microsoft.com/1A063782-2EE9-4D79-BF5D-0C160048E95E">D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS</a>. These subresources can be a subset of the render target's array slices, but you can't target subresources that aren't part of the render target view (RTV) or the depth/stencil view (DSV).


### -field Format

A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>. The data format of the resources.


### -field ResolveMode

A <a href="https://msdn.microsoft.com/1E14F62A-E6B9-4C88-AC28-2322C4662E1F">D3D12_RESOLVE_MODE</a>. The resolve operation.


### -field PreserveResolveSource

A <b>BOOL</b>. <b>TRUE</b> to preserve the resolve source, otherwise <b>FALSE</b>.

