---
UID: NF:d3d11shader.ID3D11FunctionReflection.GetResourceBindingDescByName
title: ID3D11FunctionReflection::GetResourceBindingDescByName
author: windows-sdk-content
description: Gets a description of how a resource is bound to a function.
old-location: direct3d11\id3d11functionreflection_getresourcebindingdescbyname.htm
old-project: direct3d11
ms.assetid: 4ACE2BDA-DDBE-4E22-A14F-14208693C34E
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: GetResourceBindingDescByName, GetResourceBindingDescByName method [Direct3D 11], GetResourceBindingDescByName method [Direct3D 11],ID3D11FunctionReflection interface, ID3D11FunctionReflection interface [Direct3D 11],GetResourceBindingDescByName method, ID3D11FunctionReflection.GetResourceBindingDescByName, ID3D11FunctionReflection::GetResourceBindingDescByName, d3d11shader/ID3D11FunctionReflection::GetResourceBindingDescByName, direct3d11.id3d11functionreflection_getresourcebindingdescbyname
ms.prod: windows
ms.technology: windows-sdk
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
 - ID3D11FunctionReflection.GetResourceBindingDescByName
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11FunctionReflection::GetResourceBindingDescByName


## -description


Gets a description of how a resource is bound to a function. 


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The constant-buffer name of the resource.


### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/384ad8f8-0991-4cd2-bb3d-76b8338686da">D3D11_SHADER_INPUT_BIND_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/384ad8f8-0991-4cd2-bb3d-76b8338686da">D3D11_SHADER_INPUT_BIND_DESC</a> structure that describes input binding of the resource. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. <b>GetResourceBindingDescByName</b> gets info about how one resource in the set is bound as an input to the shader. The  <i>Name</i> parameter specifies the name of the resource.




## -see-also




<a href="https://msdn.microsoft.com/91A3B6E3-E1A7-43F9-AD18-93A25F13CFB4">ID3D11FunctionReflection</a>
 

 

