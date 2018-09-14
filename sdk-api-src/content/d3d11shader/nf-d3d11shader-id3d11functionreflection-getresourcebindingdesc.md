---
UID: NF:d3d11shader.ID3D11FunctionReflection.GetResourceBindingDesc
title: ID3D11FunctionReflection::GetResourceBindingDesc
author: windows-sdk-content
description: Gets a description of how a resource is bound to a function.
old-location: direct3d11\id3d11functionreflection_getresourcebindingdesc.htm
tech.root: direct3d11
ms.assetid: A54B2CD4-BE4C-470C-BBE0-2678F659BEAF
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetResourceBindingDesc, GetResourceBindingDesc method [Direct3D 11], GetResourceBindingDesc method [Direct3D 11],ID3D11FunctionReflection interface, ID3D11FunctionReflection interface [Direct3D 11],GetResourceBindingDesc method, ID3D11FunctionReflection.GetResourceBindingDesc, ID3D11FunctionReflection::GetResourceBindingDesc, d3d11shader/ID3D11FunctionReflection::GetResourceBindingDesc, direct3d11.id3d11functionreflection_getresourcebindingdesc
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
 - ID3D11FunctionReflection.GetResourceBindingDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11FunctionReflection::GetResourceBindingDesc


## -description


Gets a description of how a resource is bound to a function. 


## -parameters




### -param ResourceIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based resource index.


### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/384ad8f8-0991-4cd2-bb3d-76b8338686da">D3D11_SHADER_INPUT_BIND_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/384ad8f8-0991-4cd2-bb3d-76b8338686da">D3D11_SHADER_INPUT_BIND_DESC</a> structure that describes input binding of the resource. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. <b>GetResourceBindingDesc</b> gets info about how one resource in the set is bound as an input to the shader. The  <i>ResourceIndex</i> parameter specifies the index for the resource.




## -see-also




<a href="https://msdn.microsoft.com/91A3B6E3-E1A7-43F9-AD18-93A25F13CFB4">ID3D11FunctionReflection</a>
 

 

