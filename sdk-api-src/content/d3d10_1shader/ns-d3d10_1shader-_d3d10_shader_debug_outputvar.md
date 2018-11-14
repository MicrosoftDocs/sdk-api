---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_OUTPUTVAR
title: "_D3D10_SHADER_DEBUG_OUTPUTVAR"
author: windows-sdk-content
description: Describes a shader output variable.
old-location: direct3d10\d3d10_shader_debug_outputvar.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_outputvar.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D10_SHADER_DEBUG_OUTPUTVAR, D3D10_SHADER_DEBUG_OUTPUTVAR structure [Direct3D 10], _D3D10_SHADER_DEBUG_OUTPUTVAR, a188f87a-61c2-dda1-1e50-d2cbcbeb680f, d3d10_1shader/D3D10_SHADER_DEBUG_OUTPUTVAR, direct3d10.d3d10_shader_debug_outputvar
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10_1shader.h
api_name:
 - D3D10_SHADER_DEBUG_OUTPUTVAR
product: Windows
targetos: Windows
req.typenames: D3D10_SHADER_DEBUG_OUTPUTVAR
req.redist: 
---

# _D3D10_SHADER_DEBUG_OUTPUTVAR structure


## -description


Describes a shader output variable.


## -struct-fields




### -field Var

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index variable being written to or if -1 it's not going to a variable.


### -field uValueMin

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Minimum UINT value.


### -field uValueMax

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Maximum UINT value.


### -field iValueMin

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Minimum INT value.


### -field iValueMax

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Maximum UINT value.


### -field fValueMin

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Minimum FLOAT value.


### -field fValueMax

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Maximum FLOAT value.


### -field bNaNPossible

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Indicates whether the output variable can evaluate to not a number.


### -field bInfPossible

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Indicates whether the output variable can evaluate to infinity.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205159(v=VS.85).aspx">Shader Structures</a>
 

 

