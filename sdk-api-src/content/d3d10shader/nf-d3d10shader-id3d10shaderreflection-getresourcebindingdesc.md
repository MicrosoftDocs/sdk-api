---
UID: NF:d3d10shader.ID3D10ShaderReflection.GetResourceBindingDesc
title: ID3D10ShaderReflection::GetResourceBindingDesc
author: windows-sdk-content
description: Get a description of the resources bound to a shader.
old-location: direct3d10\id3d10shaderreflection_getresourcebindingdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection_getresourcebindingdesc.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 6c7ed61d-9513-cb71-b3ae-307487d0a4eb, GetResourceBindingDesc, GetResourceBindingDesc method [Direct3D 10], GetResourceBindingDesc method [Direct3D 10],ID3D10ShaderReflection interface, ID3D10ShaderReflection interface [Direct3D 10],GetResourceBindingDesc method, ID3D10ShaderReflection.GetResourceBindingDesc, ID3D10ShaderReflection::GetResourceBindingDesc, d3d10shader/ID3D10ShaderReflection::GetResourceBindingDesc, direct3d10.id3d10shaderreflection_getresourcebindingdesc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Shader.h
api_name:
 - ID3D10ShaderReflection.GetResourceBindingDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10ShaderReflection::GetResourceBindingDesc


## -description


Get a description of the resources bound to a shader.


## -parameters




### -param ResourceIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based resource index.


### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/8929f7d4-6fd0-4b48-b1d8-0b089d4c730d">D3D10_SHADER_INPUT_BIND_DESC</a>*</b>

A pointer to an input-binding description. See <a href="https://msdn.microsoft.com/8929f7d4-6fd0-4b48-b1d8-0b089d4c730d">D3D10_SHADER_INPUT_BIND_DESC</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. This API gets a list of the resources that are bound as inputs to the shader.




## -see-also




<a href="https://msdn.microsoft.com/097ed643-4e7a-4214-80a1-9a56d1157044">ID3D10ShaderReflection Interface</a>
 

 

