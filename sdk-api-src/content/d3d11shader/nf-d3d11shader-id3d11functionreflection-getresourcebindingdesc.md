---
UID: NF:d3d11shader.ID3D11FunctionReflection.GetResourceBindingDesc
title: ID3D11FunctionReflection::GetResourceBindingDesc (d3d11shader.h)
author: windows-sdk-content
description: Gets a description of how a resource is bound to a function.
old-location: direct3d11\id3d11functionreflection_getresourcebindingdesc.htm
tech.root: direct3d11
ms.assetid: A54B2CD4-BE4C-470C-BBE0-2678F659BEAF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetResourceBindingDesc, GetResourceBindingDesc method [Direct3D 11], GetResourceBindingDesc method [Direct3D 11],ID3D11FunctionReflection interface, ID3D11FunctionReflection interface [Direct3D 11],GetResourceBindingDesc method, ID3D11FunctionReflection.GetResourceBindingDesc, ID3D11FunctionReflection::GetResourceBindingDesc, d3d11shader/ID3D11FunctionReflection::GetResourceBindingDesc, direct3d11.id3d11functionreflection_getresourcebindingdesc
ms.topic: method
f1_keywords: ["d3d11shader/ID3D11FunctionReflection.GetResourceBindingDesc"]
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
 - ID3D11FunctionReflection.GetResourceBindingDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11FunctionReflection::GetResourceBindingDesc


## -description


Gets a description of how a resource is bound to a function. 


## -parameters




### -param ResourceIndex [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based resource index.


### -param pDesc [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/ns-d3d11shader-_d3d11_shader_input_bind_desc">D3D11_SHADER_INPUT_BIND_DESC</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/ns-d3d11shader-_d3d11_shader_input_bind_desc">D3D11_SHADER_INPUT_BIND_DESC</a> structure that describes input binding of the resource. 


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns one of the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.




## -remarks



A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. <b>GetResourceBindingDesc</b> gets info about how one resource in the set is bound as an input to the shader. The  <i>ResourceIndex</i> parameter specifies the index for the resource.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionreflection">ID3D11FunctionReflection</a>
 

 

