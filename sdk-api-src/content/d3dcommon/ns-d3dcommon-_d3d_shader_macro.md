---
UID: NS:d3dcommon._D3D_SHADER_MACRO
title: "_D3D_SHADER_MACRO"
author: windows-sdk-content
description: Defines a shader macro.
old-location: direct3d10\d3d10_shader_macro.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_macro.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: "*LPD3D_SHADER_MACRO, 6228b971-e519-bff0-1831-d585a34e8212, D3D10_SHADER_MACRO, D3D10_SHADER_MACRO structure [Direct3D 10], D3D_SHADER_MACRO, D3D_SHADER_MACRO structure [Direct3D 10], LPD3D10_SHADER_MACRO, LPD3D10_SHADER_MACRO structure pointer [Direct3D 10], _D3D_SHADER_MACRO, d3d10shader/D3D10_SHADER_MACRO, d3d10shader/LPD3D10_SHADER_MACRO, d3dcommon/D3D10_SHADER_MACRO, d3dcommon/LPD3D10_SHADER_MACRO, direct3d10.d3d10_shader_macro"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: D3D_SHADER_MACRO, *LPD3D_SHADER_MACRO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10Shader.h
 - d3dcommon.h
api_name:
 - D3D_SHADER_MACRO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D_SHADER_MACRO structure


## -description


Defines a shader macro.


## -struct-fields




### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The macro name.


### -field Definition

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The macro definition.


## -remarks



You may use macros in your shaders. This enables the application to #define tokens at runtime, before the file is parsed. This structure defines a single macro. For example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
D3D10_SHADER_MACRO Shader_Macros[1] = { "zero", "0"  };
</pre>
</td>
</tr>
</table></span></div>
There are several shader or effect creation methods (such as <a href="https://msdn.microsoft.com/library/Bb205084(v=VS.85).aspx">D3D10CompileShader</a>, <a href="https://msdn.microsoft.com/library/Bb172658(v=VS.85).aspx">D3DX10CreateEffectFromFile</a> or <a href="https://msdn.microsoft.com/library/Bb172681(v=VS.85).aspx">D3DX10PreprocessShaderFromFile</a>) that take an array of macros as an input parameter.

The      <b>D3D10_SHADER_MACRO</b> structure is type defined in the  D3D10shader.h header file as a <a href="https://msdn.microsoft.com/8cfe0b3c-5ce8-4d59-8fd9-0fdf200c9552">D3D_SHADER_MACRO</a> structure, which is fully defined in the  D3DCommon.h header file.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef D3D_SHADER_MACRO D3D10_SHADER_MACRO;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b36309e0-1c44-42d9-adcf-33acd753438c">Shader Structures</a>
 

 

