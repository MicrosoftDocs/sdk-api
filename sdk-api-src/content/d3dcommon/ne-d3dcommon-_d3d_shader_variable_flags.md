---
UID: NE:d3dcommon._D3D_SHADER_VARIABLE_FLAGS
title: "_D3D_SHADER_VARIABLE_FLAGS"
author: windows-sdk-content
description: Flags that indicate information about a shader variable; these flags are returned using a reflection interface.
old-location: direct3d10\d3d10_shader_variable_flags.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_variable_flags.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 781d1d05-b12f-acae-af73-32340a3d5c57, D3D10_SHADER_VARIABLE_FLAGS, D3D10_SHADER_VARIABLE_FLAGS enumeration [Direct3D 10], D3D10_SVF_FORCE_DWORD, D3D10_SVF_USED, D3D10_SVF_USERPACKED, D3D11_SVF_INTERFACE_PARAMETER, D3D11_SVF_INTERFACE_POINTER, D3D_SHADER_VARIABLE_FLAGS, LPD3D10_SHADER_VARIABLE_FLAGS, LPD3D10_SHADER_VARIABLE_FLAGS enumeration pointer [Direct3D 10], _D3D_SHADER_VARIABLE_FLAGS, d3d10shader/D3D10_SHADER_VARIABLE_FLAGS, d3d10shader/D3D10_SVF_FORCE_DWORD, d3d10shader/D3D10_SVF_USED, d3d10shader/D3D10_SVF_USERPACKED, d3d10shader/D3D11_SVF_INTERFACE_PARAMETER, d3d10shader/D3D11_SVF_INTERFACE_POINTER, d3d10shader/LPD3D10_SHADER_VARIABLE_FLAGS, d3dcommon/D3D10_SHADER_VARIABLE_FLAGS, d3dcommon/D3D10_SVF_FORCE_DWORD, d3dcommon/D3D10_SVF_USED, d3dcommon/D3D10_SVF_USERPACKED, d3dcommon/D3D11_SVF_INTERFACE_PARAMETER, d3dcommon/D3D11_SVF_INTERFACE_POINTER, d3dcommon/LPD3D10_SHADER_VARIABLE_FLAGS, direct3d10.d3d10_shader_variable_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: D3D_SHADER_VARIABLE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10Shader.h
 - d3dcommon.h
api_name:
 - D3D10_SHADER_VARIABLE_FLAGS
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# _D3D_SHADER_VARIABLE_FLAGS enumeration


## -description


Flags that indicate information about a shader variable; these flags are returned using a reflection interface.


## -enum-fields




### -field D3D_SVF_USERPACKED


### -field D3D_SVF_USED


### -field D3D_SVF_INTERFACE_POINTER


### -field D3D_SVF_INTERFACE_PARAMETER


### -field D3D10_SVF_USERPACKED

Indicates that the registers assigned to this shader variable were explicitly declared in shader code (instead of automatically assigned by the compiler).


### -field D3D10_SVF_USED

Indicates that this variable is used by this shader. This value confirms that a particular shader variable (which can be common to many different shaders) is indeed used by a particular shader.


### -field D3D11_SVF_INTERFACE_POINTER

Indicates that this variable is an interface.


### -field D3D11_SVF_INTERFACE_PARAMETER

Indicates that this variable is a parameter of an interface.


### -field D3D_SVF_FORCE_DWORD




#### - D3D10_SVF_FORCE_DWORD

This value is not used by a programmer; it exists to force the enumeration to compile to 32 bits.


## -remarks



These flags are returned by a <a href="https://msdn.microsoft.com/65f57c91-955f-4383-b11c-31386e48b724">shader-variable description</a> when using shader reflection (see <a href="https://msdn.microsoft.com/18e1d597-084b-4b20-95f5-dbfe77e32944">ID3D10ShaderReflectionVariable::GetDesc</a>).

The <b>D3D10_SHADER_VARIABLE_FLAGS</b>     enumeration is type defined in the  D3D10shader.h header file as a <a href="https://msdn.microsoft.com/b89dc001-c335-4994-a644-88bfbeb7d663">D3D_SHADER_VARIABLE_FLAGS</a> enumeration, which is fully defined in the  D3DCommon.h header file.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef D3D_SHADER_VARIABLE_FLAGS D3D10_SHADER_VARIABLE_FLAGS;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8d2b758b-cc2a-43ad-bf26-51674d4b5129">Shader Enumerations</a>
 

 

