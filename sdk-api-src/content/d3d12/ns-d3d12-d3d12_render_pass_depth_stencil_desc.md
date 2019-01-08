---
UID: NS:d3d12.D3D12_RENDER_PASS_DEPTH_STENCIL_DESC
title: D3D12_RENDER_PASS_DEPTH_STENCIL_DESC
author: windows-sdk-content
description: Describes a binding (fixed for the duration of the render pass) to a depth stencil view (DSV), as well as its beginning and ending access characteristics.
old-location: direct3d12\d3d12_render_pass_depth_stencil_desc.htm
tech.root: direct3d12
ms.assetid: 1C67A6D0-F912-471F-A38C-E3C6A74303EF
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_RENDER_PASS_DEPTH_STENCIL_DESC, D3D12_RENDER_PASS_DEPTH_STENCIL_DESC structure, d3d12/D3D12_RENDER_PASS_DEPTH_STENCIL_DESC, direct3d12.d3d12_render_pass_depth_stencil_desc
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
 - D3D12_RENDER_PASS_DEPTH_STENCIL_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_RENDER_PASS_DEPTH_STENCIL_DESC
req.redist: 
---

# D3D12_RENDER_PASS_DEPTH_STENCIL_DESC structure


## -description


Describes a binding (fixed for the duration of the render pass) to a depth stencil view (DSV), as well as its beginning and ending access characteristics.


## -struct-fields




### -field cpuDescriptor

A <a href="https://msdn.microsoft.com/92451E4C-5E70-4015-8760-3F75066A44FD">D3D12_CPU_DESCRIPTOR_HANDLE</a>. The CPU descriptor handle corresponding to the depth stencil view (DSV).


### -field DepthBeginningAccess

A <a href="https://msdn.microsoft.com/48356954-F233-4FD5-A32B-099E83DC46C0">D3D12_RENDER_PASS_BEGINNING_ACCESS</a>. The access to the depth buffer requested at the transition into a render pass.


### -field StencilBeginningAccess

A <a href="https://msdn.microsoft.com/48356954-F233-4FD5-A32B-099E83DC46C0">D3D12_RENDER_PASS_BEGINNING_ACCESS</a>. The access to the stencil buffer requested at the transition into a render pass.


### -field DepthEndingAccess

A <a href="https://msdn.microsoft.com/1BEE91E3-3462-4A13-88CE-31806BC451EA">D3D12_RENDER_PASS_ENDING_ACCESS</a>. The access to the depth buffer requested at the transition out of a render pass.


### -field StencilEndingAccess

A <a href="https://msdn.microsoft.com/1BEE91E3-3462-4A13-88CE-31806BC451EA">D3D12_RENDER_PASS_ENDING_ACCESS</a>. The access to the stencil buffer requested at the transition out of a render pass.


## -see-also




<a href="/windows/desktop/direct3d12/direct3d-12-render-passes">Direct3D 12 render passes</a>
 

 

