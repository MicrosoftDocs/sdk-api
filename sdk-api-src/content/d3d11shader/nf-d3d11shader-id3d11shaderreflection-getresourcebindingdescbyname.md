---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetResourceBindingDescByName
title: ID3D11ShaderReflection::GetResourceBindingDescByName
author: windows-sdk-content
description: Get a description of how a resource is bound to a shader.
old-location: direct3d11\id3d11shaderreflection_getresourcebindingdescbyname.htm
tech.root: direct3d11
ms.assetid: b4bddcc0-c2fd-4dac-b999-cfbe1d318777
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 70b00d95-7ff3-a94d-2a18-469be48c36b3, GetResourceBindingDescByName, GetResourceBindingDescByName method [Direct3D 11], GetResourceBindingDescByName method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetResourceBindingDescByName method, ID3D11ShaderReflection.GetResourceBindingDescByName, ID3D11ShaderReflection::GetResourceBindingDescByName, d3d11shader/ID3D11ShaderReflection::GetResourceBindingDescByName, direct3d11.id3d11shaderreflection_getresourcebindingdescbyname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID3D11ShaderReflection.GetResourceBindingDescByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ShaderReflection::GetResourceBindingDescByName


## -description


Get a description of how a resource is bound to a shader. 


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCSTR</a></b>

The constant-buffer name of the resource.


### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476210(v=VS.85).aspx">D3D11_SHADER_INPUT_BIND_DESC</a>*</b>

A pointer to an input-binding description. See <a href="https://msdn.microsoft.com/en-us/library/Ff476210(v=VS.85).aspx">D3D11_SHADER_INPUT_BIND_DESC</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.




## -remarks



A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. <b>GetResourceBindingDescByName</b> gets information about how one resource in the set is bound as an input to the shader. The  <i>Name</i> parameter specifies the name of the resource.

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476590(v=VS.85).aspx">ID3D11ShaderReflection Interface</a>
 

 

