---
UID: NS:d3d12.D3D12_DISPATCH_RAYS_DESC
title: D3D12_DISPATCH_RAYS_DESC (d3d12.h)
description: Describes the properties of a ray dispatch operation initiated with a call to ID3D12GraphicsCommandList4::DispatchRays.
helpviewer_keywords: ["D3D12_DISPATCH_RAYS_DESC","D3D12_DISPATCH_RAYS_DESC structure","PD3D12_DISPATCH_RAYS_DESC","PD3D12_DISPATCH_RAYS_DESC structure pointer","d3d12/D3D12_DISPATCH_RAYS_DESC","d3d12/PD3D12_DISPATCH_RAYS_DESC","direct3d12.d3d12_dispatch_rays_desc"]
old-location: direct3d12\d3d12_dispatch_rays_desc.htm
tech.root: direct3d12
ms.assetid: F1DDFA33-A880-4AA2-AB44-43A78F086F19
ms.date: 12/05/2018
ms.keywords: D3D12_DISPATCH_RAYS_DESC, D3D12_DISPATCH_RAYS_DESC structure, PD3D12_DISPATCH_RAYS_DESC, PD3D12_DISPATCH_RAYS_DESC structure pointer, d3d12/D3D12_DISPATCH_RAYS_DESC, d3d12/PD3D12_DISPATCH_RAYS_DESC, direct3d12.d3d12_dispatch_rays_desc
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
targetos: Windows
req.typenames: D3D12_DISPATCH_RAYS_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DISPATCH_RAYS_DESC
 - d3d12/D3D12_DISPATCH_RAYS_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_DISPATCH_RAYS_DESC
---

# D3D12_DISPATCH_RAYS_DESC structure


## -description

Describes the properties of a ray dispatch operation initiated with a call to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays">ID3D12GraphicsCommandList4::DispatchRays</a>.

## -struct-fields

### -field RayGenerationShaderRecord

The shader record for the ray generation shader to use.  

The memory pointed to must be in state <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE</a>.  

The address must be aligned to 64 bytes, defined as <a href="/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_SHADER_TABLE_BYTE_ALIGNMENT</a>, and in the range [0...4096] bytes.

### -field MissShaderTable

The shader table for miss shaders.

The stride is record stride, and must be aligned to 32 bytes, defined as <a href="/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_SHADER_RECORD_BYTE_ALIGNMENT</a>, and in the range [0...4096] bytes. 0 is allowed.

The memory pointed to must be in state <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE</a>.  

The address must be aligned to 64 bytes, defined as <a href="/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_SHADER_TABLE_BYTE_ALIGNMENT</a>.

### -field HitGroupTable

The shader table for hit groups.

The stride is record stride, and must be aligned to 32 bytes, defined as <a href="/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_SHADER_RECORD_BYTE_ALIGNMENT</a>, and in the range [0...4096] bytes. 0 is allowed.

The memory pointed to must be in state <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE</a>.  

The address must be aligned to 64 bytes, defined as <a href="/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_SHADER_TABLE_BYTE_ALIGNMENT</a>.

### -field CallableShaderTable

The shader table for callable shaders.

The stride is record stride, and must be aligned to 32 bytes, defined as <a href="/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_SHADER_RECORD_BYTE_ALIGNMENT</a>. 0 is allowed.

The memory pointed to must be in state <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE</a>.  

The address must be aligned to 64 bytes, defined as <a href="/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_SHADER_TABLE_BYTE_ALIGNMENT</a>.

### -field Width

The width of the generation shader thread grid.

### -field Height

The height of the generation shader thread grid.

### -field Depth

The depth of the generation shader thread grid.