---
UID: NS:d3d12.D3D12_SHADER_RESOURCE_VIEW_DESC
title: D3D12_SHADER_RESOURCE_VIEW_DESC (d3d12.h)
description: Describes a shader-resource view. (D3D12_SHADER_RESOURCE_VIEW_DESC)
helpviewer_keywords: ["D3D12_SHADER_RESOURCE_VIEW_DESC","D3D12_SHADER_RESOURCE_VIEW_DESC structure","d3d12/D3D12_SHADER_RESOURCE_VIEW_DESC","direct3d12.d3d12_shader_resource_view_desc"]
old-location: direct3d12\d3d12_shader_resource_view_desc.htm
tech.root: direct3d12
ms.assetid: 2B4B868F-3E9F-4570-B1C7-2767ED717A3B
ms.date: 12/05/2018
ms.keywords: D3D12_SHADER_RESOURCE_VIEW_DESC, D3D12_SHADER_RESOURCE_VIEW_DESC structure, d3d12/D3D12_SHADER_RESOURCE_VIEW_DESC, direct3d12.d3d12_shader_resource_view_desc
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
req.typenames: D3D12_SHADER_RESOURCE_VIEW_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_SHADER_RESOURCE_VIEW_DESC
 - d3d12/D3D12_SHADER_RESOURCE_VIEW_DESC
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
 - D3D12_SHADER_RESOURCE_VIEW_DESC
---

## -description

Describes a shader-resource view (SRV).

## -struct-fields

### -field Format

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value that specifies the viewing format. See remarks.

### -field ViewDimension

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension">D3D12_SRV_DIMENSION</a>-typed value that specifies the resource type of the view. This type is the same as the resource type of the underlying resource. This member also determines which _SRV to use in the union below.

### -field Shader4ComponentMapping

A value, constructed using the <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_component_mapping">D3D12_ENCODE_SHADER_4_COMPONENT_MAPPING</a> macro. The **D3D12_SHADER_COMPONENT_MAPPING** enumeration specifies what values from memory should be returned when the texture is accessed in a shader via this shader resource view (SRV). For example, it can route component 1 (green) from memory, or the constant `0`, into component 2 (`.b`) of the value given to the shader.

### -field Buffer

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_srv">D3D12_BUFFER_SRV</a> structure that views the resource as a buffer.

### -field Texture1D

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_srv">D3D12_TEX1D_SRV</a> structure that views the resource as a 1D texture.

### -field Texture1DArray

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv">D3D12_TEX1D_ARRAY_SRV</a> structure that views the resource as a 1D-texture array.

### -field Texture2D

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv">D3D12_TEX2D_SRV</a> structure that views the resource as a 2D-texture.

### -field Texture2DArray

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv">D3D12_TEX2D_ARRAY_SRV</a> structure that views the resource as a 2D-texture array.

### -field Texture2DMS

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_srv">D3D12_TEX2DMS_SRV</a> structure that views the resource as a 2D-multisampled texture.

### -field Texture2DMSArray

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv">D3D12_TEX2DMS_ARRAY_SRV</a> structure that views the resource as a 2D-multisampled-texture array.

### -field Texture3D

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_srv">D3D12_TEX3D_SRV</a> structure that views the resource as a 3D texture.

### -field TextureCube

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_srv">D3D12_TEXCUBE_SRV</a> structure that views the resource as a 3D-cube texture.

### -field TextureCubeArray

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_array_srv">D3D12_TEXCUBE_ARRAY_SRV</a> structure that views the resource as a 3D-cube-texture array.

### -field RaytracingAccelerationStructure

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV</a> structure that views the resource as a raytracing acceleration structure.

## -remarks

A view is a format-specific way to look at the data in a resource. The view determines what data to look at, and how it is cast when read.

When viewing a resource, the resource-view description must specify a typed format, that is compatible with the resource format. So that means that you can't create a resource-view description using any format with _TYPELESS in the name. You can however view a typeless resource by specifying a typed format for the view. For example, a DXGI_FORMAT_R32G32B32_TYPELESS resource can be viewed with one of these typed formats: DXGI_FORMAT_R32G32B32_FLOAT, DXGI_FORMAT_R32G32B32_UINT, and DXGI_FORMAT_R32G32B32_SINT, since these typed formats are compatible with the typeless resource.

Create a shader-resource-view description by calling <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview">ID3D12Device::CreateShaderResourceView</a>.

## -see-also

[Core structures](/windows/desktop/direct3d12/direct3d-12-structures)

