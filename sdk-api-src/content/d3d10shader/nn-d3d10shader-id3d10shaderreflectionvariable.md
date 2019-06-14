---
UID: NN:d3d10shader.ID3D10ShaderReflectionVariable
title: ID3D10ShaderReflectionVariable (d3d10shader.h)
author: windows-sdk-content
description: This shader-reflection interface provides access to a variable.
old-location: direct3d10\id3d10shaderreflectionvariable.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflectionvariable.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D10ShaderReflectionVariable, ID3D10ShaderReflectionVariable interface [Direct3D 10], ID3D10ShaderReflectionVariable interface [Direct3D 10],described, d3d10shader/ID3D10ShaderReflectionVariable, direct3d10.id3d10shaderreflectionvariable, e8b67520-bfa7-7e41-f594-a51d5ad0301e
ms.topic: interface
req.header: d3d10shader.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10ShaderReflectionVariable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10ShaderReflectionVariable interface


## -description


This shader-reflection interface provides access to a variable.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10ShaderReflectionVariable</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10ShaderReflectionVariable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10ShaderReflectionVariable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflectionvariable-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get a shader-variable description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflectionvariable-gettype">GetType</a>
</td>
<td align="left" width="63%">
Get a shader-variable type.

</td>
</tr>
</table> 


## -remarks



To get a shader-reflection-variable interface, call a method like <a href="https://docs.microsoft.com/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflectionconstantbuffer-getvariablebyindex">ID3D10ShaderReflectionConstantBuffer::GetVariableByIndex</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-interfaces">Shader Interfaces</a>
 

 

