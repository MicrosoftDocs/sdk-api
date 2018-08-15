---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_VAR_INFO
title: "_D3D10_SHADER_DEBUG_VAR_INFO"
author: windows-sdk-content
description: Represents information about a shader source variable.
old-location: direct3d10\d3d10_shader_debug_var_info.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_var_info.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 0c0984a6-cb8d-ef1f-dfe5-bbc4ed81714f, D3D10_SHADER_DEBUG_VAR_INFO, D3D10_SHADER_DEBUG_VAR_INFO structure [Direct3D 10], _D3D10_SHADER_DEBUG_VAR_INFO, d3d10_1shader/D3D10_SHADER_DEBUG_VAR_INFO, direct3d10.d3d10_shader_debug_var_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10_1shader.h
req.include-header: D3D10Shader.h
req.redist: 
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
req.typenames: D3D10_SHADER_DEBUG_VAR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10_1shader.h
api_name:
 - D3D10_SHADER_DEBUG_VAR_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D10_SHADER_DEBUG_VAR_INFO structure


## -description


Represents information about a shader source variable.  


## -struct-fields




### -field TokenId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into token list for declaring identifier.


### -field Type

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172443(v=VS.85).aspx">D3D10_SHADER_VARIABLE_TYPE</a></b>

The variable type. <b>Type</b> is only required for arrays.


### -field Register

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Register the variable is stored in.


### -field Component

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The original variable that declared this variable.


### -field ScopeVar

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset into the scope variable array defined in <a href="https://msdn.microsoft.com/en-us/library/Bb172420(v=VS.85).aspx">D3D10_SHADER_DEBUG_INFO</a>.


### -field ScopeVarOffset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

This variable's offset in its <b>ScopeVar</b>.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205159(v=VS.85).aspx">Shader Structures</a>
 

 

