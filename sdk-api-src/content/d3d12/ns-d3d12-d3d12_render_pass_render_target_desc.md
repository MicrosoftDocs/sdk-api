---
UID: NS:d3d12.D3D12_RENDER_PASS_RENDER_TARGET_DESC
title: D3D12_RENDER_PASS_RENDER_TARGET_DESC (d3d12.h)
description: Describes bindings (fixed for the duration of the render pass) to one or more render target views (RTVs), as well as their beginning and ending access characteristics.helpviewer_keywords: ["D3D12_RENDER_PASS_RENDER_TARGET_DESC","D3D12_RENDER_PASS_RENDER_TARGET_DESC structure","d3d12/D3D12_RENDER_PASS_RENDER_TARGET_DESC","direct3d12.d3d12_render_pass_render_target_desc"]
old-location: direct3d12\d3d12_render_pass_render_target_desc.htm
tech.root: direct3d12
ms.assetid: C319081F-290E-4031-AE0C-F97D82ED4178
ms.date: 12/05/2018
ms.keywords: D3D12_RENDER_PASS_RENDER_TARGET_DESC, D3D12_RENDER_PASS_RENDER_TARGET_DESC structure, d3d12/D3D12_RENDER_PASS_RENDER_TARGET_DESC, direct3d12.d3d12_render_pass_render_target_desc
f1_keywords:
- d3d12/D3D12_RENDER_PASS_RENDER_TARGET_DESC
dev_langs:
- c++
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

A <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a>. The CPU descriptor handle corresponding to the render target view(s) (RTVs).


### -field BeginningAccess

A <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access">D3D12_RENDER_PASS_BEGINNING_ACCESS</a>. The access to the RTV(s) requested at the transition into a render pass.


### -field EndingAccess

A <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access">D3D12_RENDER_PASS_ENDING_ACCESS</a>. The access to the RTV(s) requested at the transition out of a render pass.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/rendering">Rendering</a>
 

 

