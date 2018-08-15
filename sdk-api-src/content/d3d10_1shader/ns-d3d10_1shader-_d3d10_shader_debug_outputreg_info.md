---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_OUTPUTREG_INFO
title: "_D3D10_SHADER_DEBUG_OUTPUTREG_INFO"
author: windows-sdk-content
description: Describes a shader output register.
old-location: direct3d10\d3d10_shader_debug_outputreg_info.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_outputreg_info.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 346fa378-bd6e-af16-a873-be0d08fda403, D3D10_SHADER_DEBUG_OUTPUTREG_INFO, D3D10_SHADER_DEBUG_OUTPUTREG_INFO structure [Direct3D 10], _D3D10_SHADER_DEBUG_OUTPUTREG_INFO, d3d10_1shader/D3D10_SHADER_DEBUG_OUTPUTREG_INFO, direct3d10.d3d10_shader_debug_outputreg_info
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
req.typenames: D3D10_SHADER_DEBUG_OUTPUTREG_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10_1shader.h
api_name:
 - D3D10_SHADER_DEBUG_OUTPUTREG_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D10_SHADER_DEBUG_OUTPUTREG_INFO structure


## -description


Describes a shader output register.


## -struct-fields




### -field OutputRegisterSet

Type: <b><a href="https://msdn.microsoft.com/62fbed9b-ca8f-4eb0-8c5d-d18ea7c76c24">D3D10_SHADER_DEBUG_REGTYPE</a></b>

Must be D3D10_SHADER_DEBUG_REG_TEMP, D3D10_SHADER_DEBUG_REG_TEMPARRAY or D3D10_SHADER_DEBUG_REG_OUTPUT.


### -field OutputReg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value of -1 indicates no output.


### -field TempArrayReg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

If <b>OutputRegisterSet</b> is D3D10_SHADER_DEBUG_REG_TEMPARRAY this indicates which temp array.


### -field OutputComponents

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value of -1 means the component is masked out.


### -field OutputVars

Type: <b><a href="https://msdn.microsoft.com/71239305-2bfa-43b2-ab5c-d6865f9ce998">D3D10_SHADER_DEBUG_OUTPUTVAR</a></b>

Indicates which variable the instruction is writing per-component.


### -field IndexReg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset from OutputReg of the element being written to. Used when writing to an indexable temp array or an output.


### -field IndexComp

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset from OutputReg of the element being written to. Used when writing to an indexable temp array or an output.


## -see-also




<a href="https://msdn.microsoft.com/b36309e0-1c44-42d9-adcf-33acd753438c">Shader Structures</a>
 

 

