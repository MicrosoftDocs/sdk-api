---
UID: NN:d3d12.ID3D12GraphicsCommandList4
title: ID3D12GraphicsCommandList4
author: windows-sdk-content
description: Represents a virtual adapter. This interface extends ID3D12Device3 to support additional features, including raytracing.
old-location: direct3d12\id3d12graphicscommandlist4.htm
tech.root: direct3d12
ms.assetid: 2385E66F-CD42-4826-B508-3EF6144179BD
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D12GraphicsCommandList4, ID3D12GraphicsCommandList4 interface, ID3D12GraphicsCommandList4 interface,described, d3d12/ID3D12GraphicsCommandList4, direct3d12.id3d12graphicscommandlist4
ms.prod: windows
ms.technology: windows-sdk
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


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Represents a virtual adapter. This interface extends <b>ID3D12Device3</b> to  support additional features, including raytracing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12GraphicsCommandList4</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12GraphicsCommandList4</b> also has these types of members:
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
<a href="direct3d12.id3d12graphicscommandlist4_buildraytracingaccelerationstructure">BuildRaytracingAccelerationStructure</a>
</td>
<td align="left" width="63%">
Performs a raytracing acceleration structure build on the GPU and optionally outputs post-build information immediately after the build.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="direct3d12.id3d12graphicscommandlist4_copyraytracingaccelerationstructure">CopyRaytracingAccelerationStructure</a>
</td>
<td align="left" width="63%">
Copies a source acceleration structure to destination memory while applying the specified transformation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="direct3d12.id3d12graphicscommandlist4_dispatchrays">DispatchRays</a>
</td>
<td align="left" width="63%">
Launch the threads of a ray generation shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="direct3d12.id3d12graphicscommandlist4_emitraytracingaccelerationstructurepostbuildinfo">EmitRaytracingAccelerationStructurePostbuildInfo</a>
</td>
<td align="left" width="63%">
Emits post-build properties for a set of acceleration structures.  This enables applications to know the output resource requirements for performing acceleration structure operations via <a href="direct3d12.id3d12graphicscommandlist4_copyraytracingaccelerationstructure">ID3D12GraphicsCommandList4::CopyRaytracingAccelerationStructure</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="direct3d12.id3d12graphicscommandlist4_setpipelinestate1">SetPipelineState1</a>
</td>
<td align="left" width="63%">
Sets a state object on the command list. 

</td>
</tr>
</table> 

