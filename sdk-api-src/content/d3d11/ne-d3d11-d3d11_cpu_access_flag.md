---
UID: NE:d3d11.D3D11_CPU_ACCESS_FLAG
title: D3D11_CPU_ACCESS_FLAG (d3d11.h)
description: Specifies the types of CPU access allowed for a resource.
helpviewer_keywords: ["D3D11_CPU_ACCESS_FLAG","D3D11_CPU_ACCESS_FLAG enumeration [Direct3D 11]","D3D11_CPU_ACCESS_READ","D3D11_CPU_ACCESS_WRITE","d3d11/D3D11_CPU_ACCESS_FLAG","d3d11/D3D11_CPU_ACCESS_READ","d3d11/D3D11_CPU_ACCESS_WRITE","direct3d11.d3d11_cpu_access_flag","e0f1ea8e-63f7-ef8a-fa11-3cbc160d2469"]
old-location: direct3d11\d3d11_cpu_access_flag.htm
tech.root: direct3d11
ms.assetid: 0a19c2a7-2570-40e2-8328-cbf5d7263605
ms.date: 12/05/2018
ms.keywords: D3D11_CPU_ACCESS_FLAG, D3D11_CPU_ACCESS_FLAG enumeration [Direct3D 11], D3D11_CPU_ACCESS_READ, D3D11_CPU_ACCESS_WRITE, d3d11/D3D11_CPU_ACCESS_FLAG, d3d11/D3D11_CPU_ACCESS_READ, d3d11/D3D11_CPU_ACCESS_WRITE, direct3d11.d3d11_cpu_access_flag, e0f1ea8e-63f7-ef8a-fa11-3cbc160d2469
req.header: d3d11.h
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
req.typenames: D3D11_CPU_ACCESS_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_CPU_ACCESS_FLAG
 - d3d11/D3D11_CPU_ACCESS_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_CPU_ACCESS_FLAG
---

# D3D11_CPU_ACCESS_FLAG enumeration


## -description

Specifies the types of CPU access allowed for a resource.

## -enum-fields

### -field D3D11_CPU_ACCESS_WRITE:0x10000L

The resource is to be mappable so that the CPU can change its contents. Resources created with this flag cannot be set as outputs of the pipeline and must be created with either dynamic or staging usage (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE</a>).

### -field D3D11_CPU_ACCESS_READ:0x20000L

The resource is to be mappable so that the CPU can read its contents. Resources created with this flag cannot be set as either inputs or outputs to the pipeline and must be created with staging usage (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE</a>).

## -remarks

This enumeration is used in <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_desc">D3D11_BUFFER_DESC</a>, <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texture1d_desc">D3D11_TEXTURE1D_DESC</a>, <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texture2d_desc">D3D11_TEXTURE2D_DESC</a>, <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texture3d_desc">D3D11_TEXTURE3D_DESC</a>. 

Applications may combine one or more of these flags with a bitwise OR. When possible, create resources with no CPU access flags, as this enables better resource optimization.

The <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_FLAG</a> cannot be used when creating resources with <b>D3D11_CPU_ACCESS</b> flags.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-enums">Resource Enumerations</a>
