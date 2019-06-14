---
UID: NN:d3d12shader.ID3D12FunctionParameterReflection
title: ID3D12FunctionParameterReflection (d3d12shader.h)
author: windows-sdk-content
description: A function-parameter-reflection interface accesses function-parameter info.
old-location: direct3d12\id3d12functionparameterreflection.htm
tech.root: direct3d12
ms.assetid: 9AB312BE-E174-46D2-BF24-32309BD88AC4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12FunctionParameterReflection, ID3D12FunctionParameterReflection interface, ID3D12FunctionParameterReflection interface,described, d3d12shader/ID3D12FunctionParameterReflection, direct3d12.id3d12functionparameterreflection
ms.topic: interface
req.header: d3d12shader.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12FunctionParameterReflection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12FunctionParameterReflection interface


## -description


A function-parameter-reflection interface accesses function-parameter info. 
          <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12FunctionParameterReflection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12FunctionParameterReflection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12FunctionParameterReflection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12functionparameterreflection-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Fills the parameter descriptor structure for the function's parameter.

</td>
</tr>
</table> 


## -remarks



To get a function-parameter-reflection interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12functionreflection-getfunctionparameter">ID3D12FunctionReflection::GetFunctionParameter</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.
      

<div class="alert"><b>Note</b>  <b>ID3D12FunctionParameterReflection</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/d3d12-graphics-reference-shader-interfaces">Shader Interfaces</a>
 

 

