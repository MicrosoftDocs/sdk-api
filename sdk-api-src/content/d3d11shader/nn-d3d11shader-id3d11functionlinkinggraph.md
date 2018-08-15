---
UID: NN:d3d11shader.ID3D11FunctionLinkingGraph
title: ID3D11FunctionLinkingGraph
author: windows-sdk-content
description: A function-linking-graph interface is used for constructing shaders that consist of a sequence of precompiled function calls that pass values to each other.
old-location: direct3d11\id3d11functionlinkinggraph.htm
old-project: direct3d11
ms.assetid: B1952085-CCD2-40F6-9A23-83B4F18FC30A
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11FunctionLinkingGraph, ID3D11FunctionLinkingGraph interface [Direct3D 11], ID3D11FunctionLinkingGraph interface [Direct3D 11],described, d3d11shader/ID3D11FunctionLinkingGraph, direct3d11.id3d11functionlinkinggraph
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11shader.h
req.include-header: 
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
req.typenames: D3D11_SHADER_VERSION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11FunctionLinkingGraph
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11FunctionLinkingGraph interface


## -description


A function-linking-graph interface is used for constructing shaders that consist of a sequence of precompiled function calls that pass values to each other. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11FunctionLinkingGraph</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11FunctionLinkingGraph</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11FunctionLinkingGraph</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0DEEE3E4-7D4E-40BD-9D96-A1C91CF5E4BE">CallFunction</a>
</td>
<td align="left" width="63%">
Creates a call-function linking node to use in the function-linking-graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7E854D31-3E34-43A7-ABEB-7FBAC94217F3">CreateModuleInstance</a>
</td>
<td align="left" width="63%">
Initializes a shader module from the function-linking-graph object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CD3B815A-0D18-4568-BCDF-7E2D5F1C139F">GenerateHlsl</a>
</td>
<td align="left" width="63%">
Generates HLSL shader code that represents the function-linking-graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5BD10944-5C49-4DA2-A2B7-73DA21A49A12">GetLastError</a>
</td>
<td align="left" width="63%">
Gets the error from the last function call of the function-linking-graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78489B91-E56D-4338-BCCB-6807EA0E8367">PassValue</a>
</td>
<td align="left" width="63%">
Passes a value from a source linking node to a destination linking node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3D74F848-A58D-4FE9-89D3-7F02A8C86A61">PassValueWithSwizzle</a>
</td>
<td align="left" width="63%">
Passes a value with swizzle from a source linking node to a destination linking node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9108BA38-6A0A-4438-BC63-A80790E4A5F0">SetInputSignature</a>
</td>
<td align="left" width="63%">
Sets the input signature of the function-linking-graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C32E3BF1-E08C-4949-A8DE-4359704D2E40">SetOutputSignature</a>
</td>
<td align="left" width="63%">
Sets the output signature of the function-linking-graph.

</td>
</tr>
</table> 


## -remarks



To get a function-linking-graph interface, call <a href="https://msdn.microsoft.com/D0BC7D62-EBF8-4144-8DC0-A87BF1B83006">D3DCreateFunctionLinkingGraph</a>. 

You can use the function-linking-graph (FLG) interface methods to construct shaders that consist of a sequence of precompiled function calls that pass values to each other. You don't need to write HLSL and then call the HLSL compiler. Instead, the shader structure is specified programmatically via a C++ API. FLG nodes represent input and output signatures and invocations of precompiled library functions. The order of registering the function-call nodes defines the sequence of invocations. You must specify the input signature node first and the output signature node last. FLG edges define how values are passed from one node to another. The data types of passed values must be the same; there is no implicit type conversion. Shape and swizzling rules follow the HLSL behavior. Values can only be passed forward in this sequence.

<div class="alert"><b>Note</b>  <b>ID3D11FunctionLinkingGraph</b> requires the D3dcompiler_47.dll or a later version of the DLL. </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

