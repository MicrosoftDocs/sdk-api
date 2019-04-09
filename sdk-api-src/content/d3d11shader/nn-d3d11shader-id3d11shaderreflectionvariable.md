---
UID: NN:d3d11shader.ID3D11ShaderReflectionVariable
title: ID3D11ShaderReflectionVariable (d3d11shader.h)
author: windows-sdk-content
description: This shader-reflection interface provides access to a variable.
old-location: direct3d11\id3d11shaderreflectionvariable.htm
tech.root: direct3d11
ms.assetid: 4422a51f-b190-4df0-a1bb-a8ee2cc66da2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11ShaderReflectionVariable, ID3D11ShaderReflectionVariable interface [Direct3D 11], ID3D11ShaderReflectionVariable interface [Direct3D 11],described, d3d11shader/ID3D11ShaderReflectionVariable, direct3d11.id3d11shaderreflectionvariable, f2ebf92b-2932-5cc0-239f-7e9b48dec05f
ms.topic: interface
req.header: d3d11shader.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11ShaderReflectionVariable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ShaderReflectionVariable interface


## -description


This shader-reflection interface provides access to a variable.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ShaderReflectionVariable</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11ShaderReflectionVariable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11ShaderReflectionVariable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E3E15010-6096-4AA5-B014-AD3054223300">GetBuffer</a>
</td>
<td align="left" width="63%">
This method returns the buffer of the current <b>ID3D11ShaderReflectionVariable</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a384e172-763f-4f4c-b6fb-f657fa31e5ee">GetDesc</a>
</td>
<td align="left" width="63%">
Get a shader-variable description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3b62396-0747-4396-ba86-9d50bfa8b529">GetInterfaceSlot</a>
</td>
<td align="left" width="63%">
Gets the corresponding interface slot for a variable that represents an interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfabd55c-0707-4221-b99e-64ef226c917e">GetType</a>
</td>
<td align="left" width="63%">
Get a shader-variable type.

</td>
</tr>
</table> 


## -remarks



To get a shader-reflection-variable interface, call a method like <a href="https://msdn.microsoft.com/8c21756f-40f0-4459-852b-445053aa03e8">ID3D11ShaderReflection::GetVariableByName</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.
          




## -see-also




<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

