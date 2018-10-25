---
UID: NN:d3d11shader.ID3D11FunctionReflection
title: ID3D11FunctionReflection
author: windows-sdk-content
description: A function-reflection interface accesses function info.
old-location: direct3d11\id3d11functionreflection.htm
tech.root: direct3d11
ms.assetid: 91A3B6E3-E1A7-43F9-AD18-93A25F13CFB4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11FunctionReflection, ID3D11FunctionReflection interface [Direct3D 11], ID3D11FunctionReflection interface [Direct3D 11],described, d3d11shader/ID3D11FunctionReflection, direct3d11.id3d11functionreflection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11shader.h
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
 - ID3D11FunctionReflection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11FunctionReflection interface


## -description


A function-reflection interface accesses function info. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11FunctionReflection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11FunctionReflection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11FunctionReflection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AFA54153-E205-4E6F-B328-9EC0262F2A5C">GetConstantBufferByIndex</a>
</td>
<td align="left" width="63%">
Gets a constant buffer by index for a function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6629A13D-4D0A-4394-9D72-F786235BEA8E">GetConstantBufferByName</a>
</td>
<td align="left" width="63%">
Gets a constant buffer by name for a function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CD4A0602-BF89-4B17-99E3-35293FB0B66C">GetDesc</a>
</td>
<td align="left" width="63%">
Fills the function descriptor structure for the function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DA2A3226-7204-4722-BCA0-74B38793A319">GetFunctionParameter</a>
</td>
<td align="left" width="63%">
Gets the function parameter reflector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A54B2CD4-BE4C-470C-BBE0-2678F659BEAF">GetResourceBindingDesc</a>
</td>
<td align="left" width="63%">
Gets a description of how a resource is bound to a function. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ACE2BDA-DDBE-4E22-A14F-14208693C34E">GetResourceBindingDescByName</a>
</td>
<td align="left" width="63%">
Gets a description of how a resource is bound to a function. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5DE3FEB3-5A5E-44E0-BBC2-52EE7FB41B2A">GetVariableByName</a>
</td>
<td align="left" width="63%">
Gets a variable by name.

</td>
</tr>
</table> 


## -remarks



To get a function-reflection interface, call <a href="https://msdn.microsoft.com/3058CCB5-E58E-4EEC-AEB9-C47B78DD6E79">ID3D11LibraryReflection::GetFunctionByIndex</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.

<div class="alert"><b>Note</b>  <b>ID3D11FunctionReflection</b> requires the D3dcompiler_47.dll or a later version of the DLL. </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

