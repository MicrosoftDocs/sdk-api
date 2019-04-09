---
UID: NE:d3d12.D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE
title: D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE (d3d12.h)
author: windows-sdk-content
description: Specifies the type of access that an application is given to the specified resource(s) at the transition into a render pass.
old-location: direct3d12\d3d12_render_pass_beginning_access_type.htm
tech.root: direct3d12
ms.assetid: 12B376DB-2CCF-493E-8B21-BAAE66B5FF1E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE, D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE enumeration, D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_CLEAR, D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_DISCARD, D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_NO_ACCESS, D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_PRESERVE, d3d12/D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE, d3d12/D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_CLEAR, d3d12/D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_DISCARD, d3d12/D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_NO_ACCESS, d3d12/D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_PRESERVE, direct3d12.d3d12_render_pass_beginning_access_type
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
 - D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE
product: Windows
targetos: Windows
req.typenames: D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE
req.redist: 
---

# D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE enumeration


## -description


Specifies the type of access that an application is given to the specified resource(s) at the transition into a render pass.


## -enum-fields




### -field D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_DISCARD

Indicates that your application doesn't have any dependency on the prior contents of the resource(s). You also shouldn't have any expectations about those contents, because a display driver may return the previously-written contents, or it may return uninitialized data. You can be assured that reading from the resource(s) won't hang the GPU, even if you do get undefined data back.
A read is defined as a traditional read from an unordered access view (UAV), a shader resource view (SRV), a constant buffer view (CBV), a vertex buffer view (VBV), an index buffer view (IBV), an IndirectArg binding/read, or a blend/depth-testing-induced read.


### -field D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_PRESERVE

Indicates that your application has a dependency on the prior contents of the resource(s), so the contents must be loaded from main memory.


### -field D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_CLEAR

Indicates that your application needs the resource(s) to be cleared to a specific value (a value that your application specifies). This clear occurs whether or not you interact with the resource(s) during the render pass. You specify the clear value at 
<a href="https://msdn.microsoft.com/6A7CF754-F2E6-48D4-8A4D-CE64B31267F7">BeginRenderPass</a> time, in the <b>Clear</b> member of your <a href="https://msdn.microsoft.com/48356954-F233-4FD5-A32B-099E83DC46C0">D3D12_RENDER_PASS_BEGINNING_ACCESS</a> structure.


### -field D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_NO_ACCESS

Indicates that your application will neither read from nor write  to the resource(s) during the render pass. You would most likely use this value to indicate that you won't be accessing the depth/stencil plane for a depth/stencil view (DSV). You must pair this value with <a href="https://msdn.microsoft.com/61B6003B-DDA5-4FF5-B1F5-994642937D29">D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_NO_ACCESS</a> in the corresponding <a href="https://msdn.microsoft.com/1BEE91E3-3462-4A13-88CE-31806BC451EA">D3D12_RENDER_PASS_ENDING_ACCESS</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/5BF1440E-E4D8-43C8-BF0E-F02FEFE79C93">Rendering</a>
 

 

