---
UID: NE:d3d10.D3D10_CPU_ACCESS_FLAG
title: D3D10_CPU_ACCESS_FLAG (d3d10.h)
description: Specifies the types of CPU access allowed for a resource.
helpviewer_keywords: ["9751a6d6-e112-7fe3-72df-bf449b5579c2","D3D10_CPU_ACCESS_FLAG","D3D10_CPU_ACCESS_FLAG enumeration [Direct3D 10]","D3D10_CPU_ACCESS_READ","D3D10_CPU_ACCESS_WRITE","d3d10/D3D10_CPU_ACCESS_FLAG","d3d10/D3D10_CPU_ACCESS_READ","d3d10/D3D10_CPU_ACCESS_WRITE","direct3d10.d3d10_cpu_access_flag"]
old-location: direct3d10\d3d10_cpu_access_flag.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_cpu_access_flag.htm
ms.date: 12/05/2018
ms.keywords: 9751a6d6-e112-7fe3-72df-bf449b5579c2, D3D10_CPU_ACCESS_FLAG, D3D10_CPU_ACCESS_FLAG enumeration [Direct3D 10], D3D10_CPU_ACCESS_READ, D3D10_CPU_ACCESS_WRITE, d3d10/D3D10_CPU_ACCESS_FLAG, d3d10/D3D10_CPU_ACCESS_READ, d3d10/D3D10_CPU_ACCESS_WRITE, direct3d10.d3d10_cpu_access_flag
req.header: d3d10.h
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
req.typenames: D3D10_CPU_ACCESS_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_CPU_ACCESS_FLAG
 - d3d10/D3D10_CPU_ACCESS_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_CPU_ACCESS_FLAG
---

# D3D10_CPU_ACCESS_FLAG enumeration


## -description

Specifies the types of CPU access allowed for a resource.

## -enum-fields

### -field D3D10_CPU_ACCESS_WRITE:0x10000L

The resource is to be <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping">mappable</a> so that the CPU can change its contents. Resources created with this flag cannot be set as outputs of the pipeline and must be created with either dynamic or staging usage (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">D3D10_USAGE</a>).

### -field D3D10_CPU_ACCESS_READ:0x20000L

The resource is to be <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping">mappable</a> so that the CPU can read its contents. Resources created with this flag cannot be set as either inputs or outputs to the pipeline and must be created with staging usage (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">D3D10_USAGE</a>).

## -remarks

This enumeration is used in <a href="/windows/desktop/api/d3d10/ns-d3d10-cd3d10_buffer_desc">D3D10_BUFFER_DESC</a>, <a href="/windows/desktop/api/d3d10/ns-d3d10-cd3d10_texture1d_desc">D3D10_TEXTURE1D_DESC</a>, <a href="/windows/desktop/api/d3d10/ns-d3d10-cd3d10_texture2d_desc">D3D10_TEXTURE2D_DESC</a>, <a href="/windows/desktop/api/d3d10/ns-d3d10-cd3d10_texture3d_desc">D3D10_TEXTURE3D_DESC</a>, and <a href="/windows/desktop/direct3d10/d3dx10-image-load-info">D3DX10_IMAGE_LOAD_INFO</a>. See <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating">Creating Buffer Resources (Direct3D 10)</a> for more details.

Applications can combine one or more of these flags with a bitwise OR. When possible, create resources with no CPU access flags, as this enables better resource optimization.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-enums">Resource Enumerations</a>
