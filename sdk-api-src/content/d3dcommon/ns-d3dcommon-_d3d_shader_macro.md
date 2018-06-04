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
 

 

