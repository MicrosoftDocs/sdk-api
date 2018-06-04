---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _D3D10_SHADER_DEBUG_REGTYPE enumeration


## -description


Shader register types.


## -enum-fields




### -field D3D10_SHADER_DEBUG_REG_INPUT

Input register.


### -field D3D10_SHADER_DEBUG_REG_OUTPUT

Output register.


### -field D3D10_SHADER_DEBUG_REG_CBUFFER

Constant buffer register.


### -field D3D10_SHADER_DEBUG_REG_TBUFFER

Texture buffer register.


### -field D3D10_SHADER_DEBUG_REG_TEMP

Temporary register.


### -field D3D10_SHADER_DEBUG_REG_TEMPARRAY

Array of temporary registers.


### -field D3D10_SHADER_DEBUG_REG_TEXTURE

Texture register.


### -field D3D10_SHADER_DEBUG_REG_SAMPLER

Sampler register.


### -field D3D10_SHADER_DEBUG_REG_IMMEDIATECBUFFER

Immediate constant buffer register.


### -field D3D10_SHADER_DEBUG_REG_LITERAL

Literal register.


### -field D3D10_SHADER_DEBUG_REG_UNUSED

Unused register.


### -field D3D11_SHADER_DEBUG_REG_INTERFACE_POINTERS

Interface register.


### -field D3D11_SHADER_DEBUG_REG_UAV

Unordered Access View (UAV) register.


### -field D3D10_SHADER_DEBUG_REG_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.


## -remarks



The <b>D3D10_SHADER_DEBUG_REGTYPE</b> enumeration is used to specify register types 
  in <a href="https://msdn.microsoft.com/143b770a-9ae0-4e2e-9d71-e0d4838070cb">D3D10_SHADER_DEBUG_INPUT_INFO</a> and <a href="https://msdn.microsoft.com/13d04629-ce71-403d-b3cb-9809715b557f">D3D10_SHADER_DEBUG_OUTPUTREG_INFO</a>.




## -see-also




<a href="https://msdn.microsoft.com/8d2b758b-cc2a-43ad-bf26-51674d4b5129">Shader Enumerations</a>
 

 

