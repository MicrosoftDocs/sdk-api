---
UID: NE:d3d12.D3D12_RENDER_PASS_ENDING_ACCESS_TYPE
title: D3D12_RENDER_PASS_ENDING_ACCESS_TYPE
author: windows-sdk-content
description: Specifies the type of access that an application is given to the specified resource(s) at the transition out of a render pass.
old-location: direct3d12\d3d12_render_pass_ending_access_type.htm
tech.root: direct3d12
ms.assetid: 61B6003B-DDA5-4FF5-B1F5-994642937D29
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_RENDER_PASS_ENDING_ACCESS_TYPE, D3D12_RENDER_PASS_ENDING_ACCESS_TYPE enumeration, D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_DISCARD, D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_NO_ACCESS, D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_PRESERVE, D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_RESOLVE, d3d12/D3D12_RENDER_PASS_ENDING_ACCESS_TYPE, d3d12/D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_DISCARD, d3d12/D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_NO_ACCESS, d3d12/D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_PRESERVE, d3d12/D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_RESOLVE, direct3d12.d3d12_render_pass_ending_access_type
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
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - D3D12_RENDER_PASS_ENDING_ACCESS_TYPE
product: Windows
targetos: Windows
req.typenames: D3D12_RENDER_PASS_ENDING_ACCESS_TYPE
req.redist: 
---

# D3D12_RENDER_PASS_ENDING_ACCESS_TYPE enumeration


## -description


Specifies the type of access that an application is given to the specified resource(s) at the transition out of a render pass.


## -enum-fields




### -field D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_DISCARD

Indicates that your application won't have any future dependency on any data that you wrote to the resource(s) during this render pass. For example, a depth buffer that won't be textured from before it's written to again.


### -field D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_PRESERVE

Indicates that your application will have a dependency on the written contents of the resource(s) in the future, and so they must be preserved.


### -field D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_RESOLVE

Indicates that the resource(s)—for example, a multi-sample anti-aliasing (MSAA) surface—should be directly resolved to a separate resource at the conclusion of the render pass. For a tile-based deferred renderer (TBDR), this should ideally happenwhile the MSAA contents are still in the tile cache. You should ensure that the resolve destination is in the <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATE_RESOLVE_DEST</a> resource state when the render pass ends. The resolve source is left in its initial resource state at the time the render pass ends.  A resolve operation submitted by a render pass doesn't implicitly change the state of any resource.


### -field D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_NO_ACCESS

Indicates that your application will neither read from nor write  to the resource(s) during the render pass. You would most likely use this value to indicate that you won't be accessing the depth/stencil plane for a depth/stencil view (DSV). You must pair this value with <a href="https://msdn.microsoft.com/12B376DB-2CCF-493E-8B21-BAAE66B5FF1E">D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_NO_ACCESS</a> in the corresponding <a href="https://msdn.microsoft.com/48356954-F233-4FD5-A32B-099E83DC46C0">D3D12_RENDER_PASS_BEGINNING_ACCESS</a> structure.


## -see-also




<a href="/windows/desktop/direct3d12/direct3d-12-render-passes">Direct3D 12 render passes</a>
 

 

