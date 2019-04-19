---
UID: NN:d3d12.ID3D12GraphicsCommandList4
title: ID3D12GraphicsCommandList4 (d3d12.h)
author: windows-sdk-content
description: Encapsulates a list of graphics commands for rendering, extending the interface to support ray tracing and render passes.
old-location: direct3d12\id3d12graphicscommandlist4.htm
tech.root: direct3d12
ms.assetid: 2385E66F-CD42-4826-B508-3EF6144179BD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList4, ID3D12GraphicsCommandList4 interface, ID3D12GraphicsCommandList4 interface,described, d3d12/ID3D12GraphicsCommandList4, direct3d12.id3d12graphicscommandlist4
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
ms.custom: 19H1
---

# ID3D12GraphicsCommandList4 interface


## -description


Encapsulates a list of graphics commands for rendering, extending the interface to support ray tracing and render passes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12GraphicsCommandList4</b> interface inherits from <a href="https://msdn.microsoft.com/934CB757-495A-45DA-A942-1852D8E94934">ID3D12GraphicsCommandList3</a>. <b>ID3D12GraphicsCommandList4</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6A7CF754-F2E6-48D4-8A4D-CE64B31267F7">BeginRenderPass</a>
</td>
<td align="left" width="63%">
Marks the beginning of a render pass by binding a set of output resources for the duration of the render pass. These bindings are to one or more render target views (RTVs), and/or to a depth stencil view (DSV).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt847461(v=VS.85).aspx">BuildRaytracingAccelerationStructure</a>
</td>
<td align="left" width="63%">
Performs a raytracing acceleration structure build on the GPU and optionally outputs post-build information immediately after the build.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt847462(v=VS.85).aspx">CopyRaytracingAccelerationStructure</a>
</td>
<td align="left" width="63%">
Copies a source acceleration structure to destination memory while applying the specified transformation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt847463(v=VS.85).aspx">DispatchRays</a>
</td>
<td align="left" width="63%">
Launch the threads of a ray generation shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt847464(v=VS.85).aspx">EmitRaytracingAccelerationStructurePostbuildInfo</a>
</td>
<td align="left" width="63%">
Emits post-build properties for a set of acceleration structures.  This enables applications to know the output resource requirements for performing acceleration structure operations via <a href="http://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure">ID3D12GraphicsCommandList4::CopyRaytracingAccelerationStructure</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6CFF2A67-F2F0-41F8-8BEC-D52003DE2767">EndRenderPass</a>
</td>
<td align="left" width="63%">
Marks the ending of a render pass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/208D3152-C0CA-40C4-A990-8815C69E73FB">ExecuteMetaCommand</a>
</td>
<td align="left" width="63%">
Records the execution (or invocation) of the specified meta command into a graphics command list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EC50FE25-27C7-4A5D-B4D1-57D402730AF0">InitializeMetaCommand</a>
</td>
<td align="left" width="63%">
Initializes the specified meta command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt847465(v=VS.85).aspx">SetPipelineState1</a>
</td>
<td align="left" width="63%">
Sets a state object on the command list. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/934CB757-495A-45DA-A942-1852D8E94934">ID3D12GraphicsCommandList3</a>
 

 

