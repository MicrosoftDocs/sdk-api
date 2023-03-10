---
UID: NE:d3d12shader.D3D12_SHADER_VERSION_TYPE
title: D3D12_SHADER_VERSION_TYPE (d3d12shader.h)
description: Enumerates the types of shaders that Direct3D recognizes. Used to encode the Version member of the D3D12_SHADER_DESC structure.
helpviewer_keywords: ["D3D12_SHADER_VERSION_TYPE","D3D12_SHADER_VERSION_TYPE enumeration","D3D12_SHVER_COMPUTE_SHADER","D3D12_SHVER_DOMAIN_SHADER","D3D12_SHVER_GEOMETRY_SHADER","D3D12_SHVER_HULL_SHADER","D3D12_SHVER_PIXEL_SHADER","D3D12_SHVER_RESERVED0","D3D12_SHVER_VERTEX_SHADER","d3d12shader/D3D12_SHADER_VERSION_TYPE","d3d12shader/D3D12_SHVER_COMPUTE_SHADER","d3d12shader/D3D12_SHVER_DOMAIN_SHADER","d3d12shader/D3D12_SHVER_GEOMETRY_SHADER","d3d12shader/D3D12_SHVER_HULL_SHADER","d3d12shader/D3D12_SHVER_PIXEL_SHADER","d3d12shader/D3D12_SHVER_RESERVED0","d3d12shader/D3D12_SHVER_VERTEX_SHADER","direct3d12.d3d12_shader_version_type"]
old-location: direct3d12\d3d12_shader_version_type.htm
tech.root: direct3d12
ms.assetid: 4691452D-3A7B-4890-AE41-B6AF5C541A3B
ms.date: 12/05/2018
ms.keywords: D3D12_SHADER_VERSION_TYPE, D3D12_SHADER_VERSION_TYPE enumeration, D3D12_SHVER_COMPUTE_SHADER, D3D12_SHVER_DOMAIN_SHADER, D3D12_SHVER_GEOMETRY_SHADER, D3D12_SHVER_HULL_SHADER, D3D12_SHVER_PIXEL_SHADER, D3D12_SHVER_RESERVED0, D3D12_SHVER_VERTEX_SHADER, d3d12shader/D3D12_SHADER_VERSION_TYPE, d3d12shader/D3D12_SHVER_COMPUTE_SHADER, d3d12shader/D3D12_SHVER_DOMAIN_SHADER, d3d12shader/D3D12_SHVER_GEOMETRY_SHADER, d3d12shader/D3D12_SHVER_HULL_SHADER, d3d12shader/D3D12_SHVER_PIXEL_SHADER, d3d12shader/D3D12_SHVER_RESERVED0, d3d12shader/D3D12_SHVER_VERTEX_SHADER, direct3d12.d3d12_shader_version_type
req.header: d3d12shader.h
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
req.typenames: D3D12_SHADER_VERSION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_SHADER_VERSION_TYPE
 - d3d12shader/D3D12_SHADER_VERSION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12shader.h
api_name:
 - D3D12_SHADER_VERSION_TYPE
---

# D3D12_SHADER_VERSION_TYPE enumeration


## -description

Enumerates the types of shaders that Direct3D recognizes.  
          Used to encode the <b>Version</b> member of the <a href="/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_desc">D3D12_SHADER_DESC</a> structure.

## -enum-fields

### -field D3D12_SHVER_PIXEL_SHADER:0

Pixel shader.

### -field D3D12_SHVER_VERTEX_SHADER:1

Vertex shader.

### -field D3D12_SHVER_GEOMETRY_SHADER:2

Geometry shader.

### -field D3D12_SHVER_HULL_SHADER:3

Hull shader.

### -field D3D12_SHVER_DOMAIN_SHADER:4

Domain shader.

### -field D3D12_SHVER_COMPUTE_SHADER:5

Compute shader.

### -field D3D12_SHVER_RESERVED0:0xFFF0

Indicates the end of the enumeration.

## -see-also

<a href="/windows/desktop/direct3d12/d3d12-graphics-reference-shader-enums">Shader Enumerations</a>
