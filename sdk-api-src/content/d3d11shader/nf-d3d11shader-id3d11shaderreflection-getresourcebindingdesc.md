---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetResourceBindingDesc
title: ID3D11ShaderReflection::GetResourceBindingDesc
author: windows-sdk-content
description: Get a description of how a resource is bound to a shader.
old-location: direct3d11\id3d11shaderreflection_getresourcebindingdesc.htm
old-project: direct3d11
ms.assetid: 2bd540f5-513d-4dd5-ab28-b0e8083231eb
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 32c283b0-2e5b-b925-599a-d35d69593ee6, GetResourceBindingDesc, GetResourceBindingDesc method [Direct3D 11], GetResourceBindingDesc method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetResourceBindingDesc method, ID3D11ShaderReflection.GetResourceBindingDesc, ID3D11ShaderReflection::GetResourceBindingDesc, d3d11shader/ID3D11ShaderReflection::GetResourceBindingDesc, direct3d11.id3d11shaderreflection_getresourcebindingdesc
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
 - ID3D11ShaderReflection.GetResourceBindingDesc
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11ShaderReflection::GetResourceBindingDesc


## -description


Get a description of how a resource is bound to a shader.


## -parameters




### -param ResourceIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based resource index.


### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/384ad8f8-0991-4cd2-bb3d-76b8338686da">D3D11_SHADER_INPUT_BIND_DESC</a>*</b>

A pointer to an input-binding description. See <a href="https://msdn.microsoft.com/384ad8f8-0991-4cd2-bb3d-76b8338686da">D3D11_SHADER_INPUT_BIND_DESC</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. <b>GetResourceBindingDesc</b> gets information about how one resource in the set is bound as an input to the shader. The  <i>ResourceIndex</i> parameter specifies the index for the resource.

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/a28cca72-7f2d-416a-bfa9-4d1f71fc98d5">ID3D11ShaderReflection Interface</a>
 

 

