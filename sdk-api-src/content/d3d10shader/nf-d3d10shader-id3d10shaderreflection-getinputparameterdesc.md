---
UID: NF:d3d10shader.ID3D10ShaderReflection.GetInputParameterDesc
title: ID3D10ShaderReflection::GetInputParameterDesc
author: windows-driver-content
description: Get an input-parameter description for a shader.
old-location: direct3d10\id3d10shaderreflection_getinputparameterdesc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection_getinputparameterdesc.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: 944856ef-d7fa-07b3-e7de-3d7d604ff3e0, GetInputParameterDesc, GetInputParameterDesc method [Direct3D 10], GetInputParameterDesc method [Direct3D 10],ID3D10ShaderReflection interface, ID3D10ShaderReflection interface [Direct3D 10],GetInputParameterDesc method, ID3D10ShaderReflection.GetInputParameterDesc, ID3D10ShaderReflection::GetInputParameterDesc, d3d10shader/ID3D10ShaderReflection::GetInputParameterDesc, direct3d10.id3d10shaderreflection_getinputparameterdesc
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
req.typenames: D3D10_MESSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10Shader.h
api_name:
-	ID3D10ShaderReflection.GetInputParameterDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10ShaderReflection::GetInputParameterDesc


## -description


Get an input-parameter description for a shader.


## -parameters




### -param ParameterIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based parameter index.


### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/4c789141-5381-4fe9-b54f-c1a2761a5a20">D3D10_SIGNATURE_PARAMETER_DESC</a>*</b>

A pointer to a shader-input-signature description. See <a href="https://msdn.microsoft.com/4c789141-5381-4fe9-b54f-c1a2761a5a20">D3D10_SIGNATURE_PARAMETER_DESC</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



An input-parameter description is also called a shader signature. The shader signature contains information about the input parameters such as the order or parameters, their data type, and a parameter semantic.




## -see-also




<a href="https://msdn.microsoft.com/097ed643-4e7a-4214-80a1-9a56d1157044">ID3D10ShaderReflection Interface</a>
 

 

