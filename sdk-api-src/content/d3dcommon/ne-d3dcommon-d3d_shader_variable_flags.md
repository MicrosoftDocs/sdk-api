---
UID: NE:d3dcommon._D3D_SHADER_VARIABLE_FLAGS
title: D3D_SHADER_VARIABLE_FLAGS (d3dcommon.h)
author: windows-sdk-content
description: Values that identify information about a shader variable.
old-location: direct3d11\d3d_shader_variable_flags.htm
tech.root: direct3d11
ms.assetid: b89dc001-c335-4994-a644-88bfbeb7d663
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D10_SVF_USED, D3D10_SVF_USERPACKED, D3D11_SVF_INTERFACE_PARAMETER, D3D11_SVF_INTERFACE_POINTER, D3D_SHADER_VARIABLE_FLAGS, D3D_SHADER_VARIABLE_FLAGS enumeration [Direct3D 11], D3D_SVF_FORCE_DWORD, D3D_SVF_INTERFACE_PARAMETER, D3D_SVF_INTERFACE_POINTER, D3D_SVF_USED, D3D_SVF_USERPACKED, d3dcommon/D3D10_SVF_USED, d3dcommon/D3D10_SVF_USERPACKED, d3dcommon/D3D11_SVF_INTERFACE_PARAMETER, d3dcommon/D3D11_SVF_INTERFACE_POINTER, d3dcommon/D3D_SHADER_VARIABLE_FLAGS, d3dcommon/D3D_SVF_FORCE_DWORD, d3dcommon/D3D_SVF_INTERFACE_PARAMETER, d3dcommon/D3D_SVF_INTERFACE_POINTER, d3dcommon/D3D_SVF_USED, d3dcommon/D3D_SVF_USERPACKED, direct3d11.d3d_shader_variable_flags
ms.topic: enum
f1_keywords:
- d3dcommon/D3D_SHADER_VARIABLE_FLAGS
dev_langs:
 - c++
req.header: d3dcommon.h
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
- D3DCommon.h
api_name:
- D3D_SHADER_VARIABLE_FLAGS
targetos: Windows
req.typenames: D3D_SHADER_VARIABLE_FLAGS
req.redist: 
ms.custom: 19H1
---

# D3D_SHADER_VARIABLE_FLAGS enumeration


## -description


Values that identify information about a shader variable.


## -enum-fields




### -field D3D_SVF_USERPACKED

Indicates that the registers assigned to this shader variable were explicitly declared in shader code (instead of automatically assigned by the compiler).


### -field D3D_SVF_USED

Indicates that this variable is used by this shader. This value confirms that a particular shader variable (which can be common to many different shaders) is indeed used by a particular shader.


### -field D3D_SVF_INTERFACE_POINTER

Indicates that this variable is an interface.


### -field D3D_SVF_INTERFACE_PARAMETER

Indicates that this variable is a parameter of an interface.


### -field D3D10_SVF_USERPACKED

Indicates that the registers assigned to this shader variable were explicitly declared in shader code (instead of automatically assigned by the compiler).


### -field D3D10_SVF_USED

Indicates that this variable is used by this shader. This value confirms that a particular shader variable (which can be common to many different shaders) is indeed used by a particular shader.


### -field D3D11_SVF_INTERFACE_POINTER

Indicates that this variable is an interface.


### -field D3D11_SVF_INTERFACE_PARAMETER

Indicates that this variable is a parameter of an interface.


### -field D3D_SVF_FORCE_DWORD

This value is not used by a programmer; it exists to force the enumeration to compile to 32 bits.


## -remarks



A call to the  <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc">ID3D11ShaderReflectionVariable::GetDesc</a> method returns <b>D3D_SHADER_VARIABLE_FLAGS</b> values in the  <b>uFlags</b> member of a  <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc">D3D11_SHADER_VARIABLE_DESC</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-common-enumerations">Common Version Enumerations</a>
 

 

