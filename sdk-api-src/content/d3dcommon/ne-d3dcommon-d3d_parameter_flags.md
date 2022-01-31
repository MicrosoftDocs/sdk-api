---
UID: NE:d3dcommon._D3D_PARAMETER_FLAGS
title: D3D_PARAMETER_FLAGS (d3dcommon.h)
description: Indicates semantic flags for function parameters.
helpviewer_keywords: ["D3D_PARAMETER_FLAGS","D3D_PARAMETER_FLAGS enumeration [Direct3D 11]","D3D_PF_FORCE_DWORD","D3D_PF_IN","D3D_PF_NONE","D3D_PF_OUT","d3dcommon/D3D_PARAMETER_FLAGS","d3dcommon/D3D_PF_FORCE_DWORD","d3dcommon/D3D_PF_IN","d3dcommon/D3D_PF_NONE","d3dcommon/D3D_PF_OUT","direct3d11.d3d_parameter_flags"]
old-location: direct3d11\d3d_parameter_flags.htm
tech.root: direct3d11
ms.assetid: 36D757E7-2960-43E3-8C5E-8B11F0109ACD
ms.date: 12/05/2018
ms.keywords: D3D_PARAMETER_FLAGS, D3D_PARAMETER_FLAGS enumeration [Direct3D 11], D3D_PF_FORCE_DWORD, D3D_PF_IN, D3D_PF_NONE, D3D_PF_OUT, d3dcommon/D3D_PARAMETER_FLAGS, d3dcommon/D3D_PF_FORCE_DWORD, d3dcommon/D3D_PF_IN, d3dcommon/D3D_PF_NONE, d3dcommon/D3D_PF_OUT, direct3d11.d3d_parameter_flags
req.header: d3dcommon.h
req.include-header: D3D11Shader.h
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
req.typenames: D3D_PARAMETER_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D_PARAMETER_FLAGS
 - d3dcommon/_D3D_PARAMETER_FLAGS
 - D3D_PARAMETER_FLAGS
 - d3dcommon/D3D_PARAMETER_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dcommon.h
api_name:
 - D3D_PARAMETER_FLAGS
---

# D3D_PARAMETER_FLAGS enumeration


## -description

Indicates semantic flags for function parameters.

## -enum-fields

### -field D3D_PF_NONE:0

The parameter has no semantic flags.

### -field D3D_PF_IN:0x1

Indicates an input parameter.

### -field D3D_PF_OUT:0x2

Indicates an output parameter.

### -field D3D_PF_FORCE_DWORD:0x7fffffff

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.

## -see-also

<a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc">D3D11_PARAMETER_DESC</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-enums">Shader Enumerations</a>
