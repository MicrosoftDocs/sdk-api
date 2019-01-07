---
UID: NE:d3d12.D3D12_RENDER_PASS_TIER
title: D3D12_RENDER_PASS_TIER
author: windows-sdk-content
description: Specifies the level of support for render passes on a graphics device.
old-location: direct3d12\d3d12_render_pass_tier.htm
tech.root: direct3d12
ms.assetid: 8EBAFE04-E8C9-4BAA-8A1E-DF2BB8E4B254
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_RENDER_PASS_TIER, D3D12_RENDER_PASS_TIER enumeration, D3D12_RENDER_PASS_TIER_0, D3D12_RENDER_PASS_TIER_1, D3D12_RENDER_PASS_TIER_2, d3d12/D3D12_RENDER_PASS_TIER, d3d12/D3D12_RENDER_PASS_TIER_0, d3d12/D3D12_RENDER_PASS_TIER_1, d3d12/D3D12_RENDER_PASS_TIER_2, direct3d12.d3d12_render_pass_tier
ms.topic: enum
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
 - D3D12_RENDER_PASS_TIER
product: Windows
targetos: Windows
req.typenames: D3D12_RENDER_PASS_TIER
req.redist: 
---

# D3D12_RENDER_PASS_TIER enumeration


## -description


Specifies the level of support for render passes on a graphics device.


## -enum-fields




### -field D3D12_RENDER_PASS_TIER_0

The user-mode display driver hasn't implemented render passes, and so the feature is provided only via software emulation. Render passes might not provide a performance at this level of support.


### -field D3D12_RENDER_PASS_TIER_1

The render passes feature is implemented by the user-mode display driver, and render target/depth buffer writes may be accelerated. Unordered access view (UAV) writes are not efficiently supported within the render pass.


### -field D3D12_RENDER_PASS_TIER_2

The render passes feature is implemented by the user-mode display driver, render target/depth buffer writes may be accelerated, and unordered access view (UAV) writes (provided that writes in a render pass are not read until a subsequent render pass) are likely to be more efficient than issuing the same work without using a render pass.


## -remarks



To determine the level of support for render passes for a graphics device, pass <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE_D3D12_OPTIONS5</a> to <a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">ID3D12Device::CheckFeatureSupport</a> to retrieve a <a href="https://msdn.microsoft.com/en-us/library/Mt830391(v=VS.85).aspx">D3D12_FEATURE_DATA_D3D12_OPTIONS5</a> struct.




## -see-also




<a href="/windows/desktop/direct3d12/direct3d-12-render-passes">Direct3D 12 render passes</a>
 

 

