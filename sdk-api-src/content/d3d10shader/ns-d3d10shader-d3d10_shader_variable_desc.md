---
UID: NS:d3d10shader._D3D10_SHADER_VARIABLE_DESC
title: D3D10_SHADER_VARIABLE_DESC (d3d10shader.h)
author: windows-sdk-content
description: Describes a shader variable.
old-location: direct3d10\d3d10_shader_variable_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_variable_desc.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 93d99a1e-6d9e-3991-2e0b-086cd3eee8c0, D3D10_SHADER_VARIABLE_DESC, D3D10_SHADER_VARIABLE_DESC structure [Direct3D 10], d3d10shader/D3D10_SHADER_VARIABLE_DESC, direct3d10.d3d10_shader_variable_desc
ms.topic: struct
req.header: d3d10shader.h
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
 - D3D10Shader.h
api_name:
 - D3D10_SHADER_VARIABLE_DESC
product: Windows
targetos: Windows
req.typenames: D3D10_SHADER_VARIABLE_DESC
req.redist: 
---

# D3D10_SHADER_VARIABLE_DESC structure


## -description


Describes a shader variable.


## -struct-fields




### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The variable name.


### -field StartOffset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset from the start of the parent structure, to the beginning of the variable.


### -field Size

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the variable (in bytes).


### -field uFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags, which identify shader-variable properties (see <a href="https://msdn.microsoft.com/en-us/library/Bb172442(v=VS.85).aspx">D3D10_SHADER_VARIABLE_FLAGS</a>).


### -field DefaultValue

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPVOID</a></b>

The default value for initializing the variable.


## -remarks



Get a shader-variable description using reflection, by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173846(v=VS.85).aspx">ID3D10ShaderReflectionVariable::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205159(v=VS.85).aspx">Shader Structures</a>
 

 

