---
UID: NS:d3d12.D3D12_RENDER_PASS_RENDER_TARGET_DESC
title: D3D12_RENDER_PASS_RENDER_TARGET_DESC (d3d12.h)
author: windows-sdk-content
description: Describes bindings (fixed for the duration of the render pass) to one or more render target views (RTVs), as well as their beginning and ending access characteristics.
old-location: direct3d12\d3d12_render_pass_render_target_desc.htm
tech.root: direct3d12
ms.assetid: C319081F-290E-4031-AE0C-F97D82ED4178
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
---

# D3D12_RENDER_PASS_RENDER_TARGET_DESC structure


## -description


Describes bindings (fixed for the duration of the render pass) to one or more render target views (RTVs), as well as their beginning and ending access characteristics.


## -struct-fields




### -field cpuDescriptor

A <a href="https://msdn.microsoft.com/92451E4C-5E70-4015-8760-3F75066A44FD">D3D12_CPU_DESCRIPTOR_HANDLE</a>. The CPU descriptor handle corresponding to the render target view(s) (RTVs).


### -field BeginningAccess

A <a href="https://docs.microsoft.com/en-us/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access">D3D12_RENDER_PASS_BEGINNING_ACCESS</a>. The access to the RTV(s) requested at the transition into a render pass.


### -field EndingAccess

A <a href="https://docs.microsoft.com/en-us/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access">D3D12_RENDER_PASS_ENDING_ACCESS</a>. The access to the RTV(s) requested at the transition out of a render pass.


## -see-also




<a href="https://msdn.microsoft.com/5BF1440E-E4D8-43C8-BF0E-F02FEFE79C93">Rendering</a>
 

 

