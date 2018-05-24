---
UID: NS:d3d10shader._D3D10_SHADER_VARIABLE_DESC
title: "_D3D10_SHADER_VARIABLE_DESC"
author: windows-driver-content
description: Describes a shader variable.
old-location: direct3d10\d3d10_shader_variable_desc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_variable_desc.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: 93d99a1e-6d9e-3991-2e0b-086cd3eee8c0, D3D10_SHADER_VARIABLE_DESC, D3D10_SHADER_VARIABLE_DESC structure [Direct3D 10], _D3D10_SHADER_VARIABLE_DESC, d3d10shader/D3D10_SHADER_VARIABLE_DESC, direct3d10.d3d10_shader_variable_desc
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D10_SHADER_VARIABLE_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D10Shader.h
api_name:
-	D3D10_SHADER_VARIABLE_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D10_SHADER_VARIABLE_DESC structure


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

Flags, which identify shader-variable properties (see <a href="https://msdn.microsoft.com/e9ec8a60-c580-4aeb-abd0-5647c72e2121">D3D10_SHADER_VARIABLE_FLAGS</a>).


### -field DefaultValue

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPVOID</a></b>

The default value for initializing the variable.


## -remarks



Get a shader-variable description using reflection, by calling <a href="https://msdn.microsoft.com/18e1d597-084b-4b20-95f5-dbfe77e32944">ID3D10ShaderReflectionVariable::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/b36309e0-1c44-42d9-adcf-33acd753438c">Shader Structures</a>
 

 

