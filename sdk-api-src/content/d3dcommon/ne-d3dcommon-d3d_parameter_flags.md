---
UID: NE:d3dcommon._D3D_PARAMETER_FLAGS
title: D3D_PARAMETER_FLAGS (d3dcommon.h)
author: windows-sdk-content
description: Indicates semantic flags for function parameters.
old-location: direct3d11\d3d_parameter_flags.htm
tech.root: direct3d11
ms.assetid: 36D757E7-2960-43E3-8C5E-8B11F0109ACD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D_PARAMETER_FLAGS, D3D_PARAMETER_FLAGS enumeration [Direct3D 11], D3D_PF_FORCE_DWORD, D3D_PF_IN, D3D_PF_NONE, D3D_PF_OUT, d3dcommon/D3D_PARAMETER_FLAGS, d3dcommon/D3D_PF_FORCE_DWORD, d3dcommon/D3D_PF_IN, d3dcommon/D3D_PF_NONE, d3dcommon/D3D_PF_OUT, direct3d11.d3d_parameter_flags
ms.topic: enum
f1_keywords: ["d3dcommon/D3D_PARAMETER_FLAGS"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dcommon.h
api_name:
 - D3D_PARAMETER_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D_PARAMETER_FLAGS
req.redist: 
ms.custom: 19H1
---

# D3D_PARAMETER_FLAGS enumeration


## -description


Indicates semantic flags for function parameters.


## -enum-fields




### -field D3D_PF_NONE

The parameter has no semantic flags.


### -field D3D_PF_IN

Indicates an input parameter.


### -field D3D_PF_OUT

Indicates an output parameter.


### -field D3D_PF_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/ns-d3d11shader-_d3d11_parameter_desc">D3D11_PARAMETER_DESC</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-shader-enums">Shader Enumerations</a>
 

 

