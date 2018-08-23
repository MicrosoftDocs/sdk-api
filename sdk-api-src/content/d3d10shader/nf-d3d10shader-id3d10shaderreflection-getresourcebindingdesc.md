---
UID: NF:d3d10shader.ID3D10ShaderReflection.GetResourceBindingDesc
title: ID3D10ShaderReflection::GetResourceBindingDesc
author: windows-sdk-content
description: Get a description of the resources bound to a shader.
old-location: direct3d10\id3d10shaderreflection_getresourcebindingdesc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection_getresourcebindingdesc.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 6c7ed61d-9513-cb71-b3ae-307487d0a4eb, GetResourceBindingDesc, GetResourceBindingDesc method [Direct3D 10], GetResourceBindingDesc method [Direct3D 10],ID3D10ShaderReflection interface, ID3D10ShaderReflection interface [Direct3D 10],GetResourceBindingDesc method, ID3D10ShaderReflection.GetResourceBindingDesc, ID3D10ShaderReflection::GetResourceBindingDesc, d3d10shader/ID3D10ShaderReflection::GetResourceBindingDesc, direct3d10.id3d10shaderreflection_getresourcebindingdesc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10shader.h
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
req.typenames: D3D10_MESSAGE
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
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10ShaderReflection::GetResourceBindingDesc


## -description


Get a description of the resources bound to a shader.


## -parameters




### -param ResourceIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based resource index.


### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172433(v=VS.85).aspx">D3D10_SHADER_INPUT_BIND_DESC</a>*</b>

A pointer to an input-binding description. See <a href="https://msdn.microsoft.com/en-us/library/Bb172433(v=VS.85).aspx">D3D10_SHADER_INPUT_BIND_DESC</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. This API gets a list of the resources that are bound as inputs to the shader.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173835(v=VS.85).aspx">ID3D10ShaderReflection Interface</a>
 

 

