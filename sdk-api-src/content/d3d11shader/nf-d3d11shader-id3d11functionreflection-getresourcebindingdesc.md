---
UID: NF:d3d11shader.ID3D11FunctionReflection.GetResourceBindingDesc
title: ID3D11FunctionReflection::GetResourceBindingDesc
author: windows-sdk-content
description: Gets a description of how a resource is bound to a function.
old-location: direct3d11\id3d11functionreflection_getresourcebindingdesc.htm
old-project: direct3d11
ms.assetid: A54B2CD4-BE4C-470C-BBE0-2678F659BEAF
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetResourceBindingDesc, GetResourceBindingDesc method [Direct3D 11], GetResourceBindingDesc method [Direct3D 11],ID3D11FunctionReflection interface, ID3D11FunctionReflection interface [Direct3D 11],GetResourceBindingDesc method, ID3D11FunctionReflection.GetResourceBindingDesc, ID3D11FunctionReflection::GetResourceBindingDesc, d3d11shader/ID3D11FunctionReflection::GetResourceBindingDesc, direct3d11.id3d11functionreflection_getresourcebindingdesc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - ID3D11FunctionReflection.GetResourceBindingDesc
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11FunctionReflection::GetResourceBindingDesc


## -description


Gets a description of how a resource is bound to a function. 


## -parameters




### -param ResourceIndex [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

A zero-based resource index.


### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476210(v=VS.85).aspx">D3D11_SHADER_INPUT_BIND_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Ff476210(v=VS.85).aspx">D3D11_SHADER_INPUT_BIND_DESC</a> structure that describes input binding of the resource. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.




## -remarks



A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. <b>GetResourceBindingDesc</b> gets info about how one resource in the set is bound as an input to the shader. The  <i>ResourceIndex</i> parameter specifies the index for the resource.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn280546(v=VS.85).aspx">ID3D11FunctionReflection</a>
 

 

