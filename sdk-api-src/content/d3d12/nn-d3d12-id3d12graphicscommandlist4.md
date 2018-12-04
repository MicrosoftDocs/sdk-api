---
UID: NN:d3d12.ID3D12GraphicsCommandList4
title: ID3D12GraphicsCommandList4
author: windows-sdk-content
description: Encapsulates a list of graphics commands for rendering, extending the interface to support ray tracing and render passes.
old-location: direct3d12\id3d12graphicscommandlist4.htm
tech.root: direct3d12
ms.assetid: 2385E66F-CD42-4826-B508-3EF6144179BD
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ID3D12GraphicsCommandList4, ID3D12GraphicsCommandList4 interface, ID3D12GraphicsCommandList4 interface,described, d3d12/ID3D12GraphicsCommandList4, direct3d12.id3d12graphicscommandlist4
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12GraphicsCommandList4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList4 interface


## -description


Encapsulates a list of graphics commands for rendering, extending the interface to support ray tracing and render passes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12GraphicsCommandList4</b> interface inherits from <a href="direct3d12.id3d12graphicscommandlist3">ID3D12GraphicsCommandList3</a>. <b>ID3D12GraphicsCommandList4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12GraphicsCommandList4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="direct3d12.id3d12graphicscommandlist4_beginrenderpass">BeginRenderPass</a>
</td>
<td align="left" width="63%">
Marks the beginning of a render pass by binding a set of output resources for the duration of the render pass. These bindings are to one or more render target views (RTVs), and/or to a depth stencil view (DSV).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B714530C-40E6-4C67-8908-373BB26E6635">BuildRaytracingAccelerationStructure</a>
</td>
<td align="left" width="63%">
Performs a raytracing acceleration structure build on the GPU and optionally outputs post-build information immediately after the build.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13E0E477-9CD5-484B-9532-AB6D415CF6CB">CopyRaytracingAccelerationStructure</a>
</td>
<td align="left" width="63%">
Copies a source acceleration structure to destination memory while applying the specified transformation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/157F4609-B9AF-40EC-A2E6-33D5A897A813">DispatchRays</a>
</td>
<td align="left" width="63%">
Launch the threads of a ray generation shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05E4B38B-1A3A-4121-8BD7-A437534C8B9A">EmitRaytracingAccelerationStructurePostbuildInfo</a>
</td>
<td align="left" width="63%">
Emits post-build properties for a set of acceleration structures.  This enables applications to know the output resource requirements for performing acceleration structure operations via <a href="http://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure">ID3D12GraphicsCommandList4::CopyRaytracingAccelerationStructure</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="direct3d12.id3d12graphicscommandlist4_endrenderpass">EndRenderPass</a>
</td>
<td align="left" width="63%">
Marks the ending of a render pass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CD408074-2B2A-461C-9CA8-DC967BC61067">SetPipelineState1</a>
</td>
<td align="left" width="63%">
Sets a state object on the command list. 

</td>
</tr>
</table> 


## -see-also




<a href="direct3d12.id3d12graphicscommandlist3">ID3D12GraphicsCommandList3</a>
 

 

