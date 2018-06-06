---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_INPUT_INFO
title: "_D3D10_SHADER_DEBUG_INPUT_INFO"
author: windows-sdk-content
description: Describes a shader input.
old-location: direct3d10\d3d10_shader_debug_input_info.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_input_info.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 985acea2-3d0c-4a4c-f9db-ed556aec5b34, D3D10_SHADER_DEBUG_INPUT_INFO, D3D10_SHADER_DEBUG_INPUT_INFO structure [Direct3D 10], _D3D10_SHADER_DEBUG_INPUT_INFO, d3d10_1shader/D3D10_SHADER_DEBUG_INPUT_INFO, direct3d10.d3d10_shader_debug_input_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10_1shader.h
req.include-header: D3D10Shader.h
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
req.typenames: D3D10_SHADER_DEBUG_INPUT_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10_1shader.h
api_name:
 - D3D10_SHADER_DEBUG_INPUT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D10_SHADER_DEBUG_INPUT_INFO structure


## -description


Describes a shader input.


## -struct-fields




### -field Var

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into array of variables to initialize.


### -field InitialRegisterSet

Type: <b><a href="https://msdn.microsoft.com/62fbed9b-ca8f-4eb0-8c5d-d18ea7c76c24">D3D10_SHADER_DEBUG_REGTYPE</a></b>

Must be D3D10_SHADER_DEBUG_REG_INPUT, D3D10_SHADER_DEBUG_REG_CBUFFER or D3D10_SHADER_DEBUG_REG_TBUFFER.


### -field InitialBank

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Will contain a cbuffer or tbuffer slot, geometry shader input primitive number, identifying register for an indexable temp, or -1.


### -field InitialRegister

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Register in register set.  <b>InitialRegister</b> will be -1 if it is temporary.


### -field InitialComponent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Gives the component.  <b>InitialComponent</b> will be -1 it is temporary.


### -field InitialValue

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Initial value if the variable is a literal.


## -remarks



The <b>D3D10_SHADER_DEBUG_INPUT_INFO</b> structure is used with the <a href="https://msdn.microsoft.com/b1b4201a-5bfb-4fce-ba51-64f7da9531bc">D3D10_SHADER_DEBUG_INFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/b36309e0-1c44-42d9-adcf-33acd753438c">Shader Structures</a>
 

 

