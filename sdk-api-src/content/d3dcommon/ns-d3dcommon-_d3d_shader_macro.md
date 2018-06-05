---
UID: NS:d3dcommon._D3D_SHADER_MACRO
title: "_D3D_SHADER_MACRO"
author: windows-sdk-content
description: Defines a shader macro.
old-location: direct3d11\d3d_shader_macro.htm
old-project: direct3d11
ms.assetid: 8cfe0b3c-5ce8-4d59-8fd9-0fdf200c9552
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: "*LPD3D_SHADER_MACRO, D3D_SHADER_MACRO, D3D_SHADER_MACRO structure [Direct3D 11], LPD3D_SHADER_MACRO, LPD3D_SHADER_MACRO structure pointer [Direct3D 11], _D3D_SHADER_MACRO, d3dcommon/D3D_SHADER_MACRO, d3dcommon/LPD3D_SHADER_MACRO, direct3d11.d3d_shader_macro"
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
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3DCommon.h
api_name:
-	D3D_SHADER_MACRO
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

The macro name.


### -field Definition

The macro definition.


## -remarks



You can use shader macros in your shaders. The <b>D3D_SHADER_MACRO</b> structure defines a single shader macro as shown in the following example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
D3D_SHADER_MACRO Shader_Macros[] = { "zero", "0", NULL, NULL };
</pre>
</td>
</tr>
</table></span></div>
The following shader or effect creation functions take an array of shader macros as an input parameter:

<ul>
<li>
<a href="https://msdn.microsoft.com/c81b06ba-129a-468e-8f39-a9ed7f9368b1">D3D10CompileShader</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1418857e-bda1-4ffb-bbb9-dfa3709313b1">D3DX10CreateEffectFromFile</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9f609aa5-5ee7-45fb-9693-69de130b6cc0">D3DX10PreprocessShaderFromFile</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a7e9754b-acc1-49d0-bd8e-b116bc3c7e3a">D3DX11CreateAsyncShaderPreprocessProcessor</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/d18f5baa-ef4e-41bc-90f2-28788faeb39d">Common Version Structures</a>
 

 

