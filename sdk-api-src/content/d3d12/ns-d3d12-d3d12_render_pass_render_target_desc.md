---
UID: NS:d3d12.D3D12_RENDER_PASS_RENDER_TARGET_DESC
title: D3D12_RENDER_PASS_RENDER_TARGET_DESC
author: windows-sdk-content
description: Describes bindings (fixed for the duration of the render pass) to one or more render target views (RTVs), as well as their beginning and ending access characteristics.
old-location: direct3d12\d3d12_render_pass_render_target_desc.htm
tech.root: direct3d12
ms.assetid: C319081F-290E-4031-AE0C-F97D82ED4178
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_RENDER_PASS_RENDER_TARGET_DESC, D3D12_RENDER_PASS_RENDER_TARGET_DESC structure, d3d12/D3D12_RENDER_PASS_RENDER_TARGET_DESC, direct3d12.d3d12_render_pass_render_target_desc
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
 - D3D12_RENDER_PASS_RENDER_TARGET_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_RENDER_PASS_RENDER_TARGET_DESC
req.redist: 
---

# D3D12_RENDER_PASS_RENDER_TARGET_DESC structure


## -description


Describes bindings (fixed for the duration of the render pass) to one or more render target views (RTVs), as well as their beginning and ending access characteristics.


## -struct-fields




### -field cpuDescriptor

A <a href="https://msdn.microsoft.com/92451E4C-5E70-4015-8760-3F75066A44FD">D3D12_CPU_DESCRIPTOR_HANDLE</a>. The CPU descriptor handle corresponding to the render target view(s) (RTVs).


### -field BeginningAccess

A <a href="https://msdn.microsoft.com/48356954-F233-4FD5-A32B-099E83DC46C0">D3D12_RENDER_PASS_BEGINNING_ACCESS</a>. The access to the RTV(s) requested at the transition into a render pass.


### -field EndingAccess

A <a href="https://msdn.microsoft.com/1BEE91E3-3462-4A13-88CE-31806BC451EA">D3D12_RENDER_PASS_ENDING_ACCESS</a>. The access to the RTV(s) requested at the transition out of a render pass.

