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
ms.custom: 19H1
---

# ID3D11ShaderReflectionVariable interface


## -description


This shader-reflection interface provides access to a variable.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ShaderReflectionVariable</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11ShaderReflectionVariable</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getbuffer">GetBuffer</a>
</td>
<td align="left" width="63%">
This method returns the buffer of the current <b>ID3D11ShaderReflectionVariable</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get a shader-variable description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot">GetInterfaceSlot</a>
</td>
<td align="left" width="63%">
Gets the corresponding interface slot for a variable that represents an interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-gettype">GetType</a>
</td>
<td align="left" width="63%">
Get a shader-variable type.

</td>
</tr>
</table> 


## -remarks



To get a shader-reflection-variable interface, call a method like <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname">ID3D11ShaderReflection::GetVariableByName</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
 

 

