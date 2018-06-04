---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _D3D10_SIGNATURE_PARAMETER_DESC structure


## -description


Describes a shader signature.


## -struct-fields




### -field SemanticName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

A per-parameter string that identifies how the data will be used. See <a href="https://msdn.microsoft.com/6f5c504c-1940-4d1c-b594-a2132599376b">Semantics (DirectX HLSL)</a>.


### -field SemanticIndex

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Semantic index that modifies the semantic. Used to differentiate different parameters that use the same semantic.


### -field Register

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The register that will contain this variable's data.


### -field SystemValueType

Type: <b><a href="https://msdn.microsoft.com/a01317cd-5f6f-4104-9818-87beaf00cddb">D3D10_NAME</a></b>

A predefined string that determines the functionality of certain pipeline stages. See <a href="https://msdn.microsoft.com/a01317cd-5f6f-4104-9818-87beaf00cddb">D3D10_NAME</a>.


### -field ComponentType

Type: <b><a href="https://msdn.microsoft.com/410ea42e-fc10-4c14-b0fc-446dc5b6d64f">D3D10_REGISTER_COMPONENT_TYPE</a></b>

The per-component-data type that is stored in a register. See <a href="https://msdn.microsoft.com/410ea42e-fc10-4c14-b0fc-446dc5b6d64f">D3D10_REGISTER_COMPONENT_TYPE</a>. Each register can store up to four-components of data.


### -field Mask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Mask which indicates which components of a register are used.


### -field ReadWriteMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Mask which indicates whether a given component is never written (if the signature is an output signature) or always read (if the signature is an input signature). The mask is a combination of <a href="https://msdn.microsoft.com/410ea42e-fc10-4c14-b0fc-446dc5b6d64f">D3D10_REGISTER_COMPONENT_TYPE</a> values.


## -remarks



A shader can take n inputs and can produce m outputs. The order of the input (or output) parameters, their associated types, and any attached semantics make up the shader signature. Each shader has an input and an output signature.

When compiling a shader or an effect, some API calls validate shader signatures (such as <a href="https://msdn.microsoft.com/c81b06ba-129a-468e-8f39-a9ed7f9368b1">D3D10CompileShader</a> and <a href="https://msdn.microsoft.com/21f6fdaf-2da9-4bb4-8bb8-8c4b2d0cf07a">D3D10CompileEffectFromMemory</a>). That is, they compare the output signature of one shader (like a vertex shader) with the input signature of another shader (like a pixel shader). This ensures that a shader outputs data that is compatible with a downstream shader that is consuming that data. Compatible means that a shader signature is a exact-match subset of the preceding shader stage. Exact match means parameter types and semantics must exactly match. Subset means that a parameter that is not required by a downstream stage, does not need to include that parameter in its shader signature.

Get a shader-signature from a shader or an effect by calling APIs such as <a href="https://msdn.microsoft.com/40f06537-d058-420d-88aa-7052c2488e33">ID3D10ShaderReflection::GetInputParameterDesc</a> or <a href="https://msdn.microsoft.com/f76326ff-4de3-4cd7-b398-9141196cfd2a">ID3D10EffectShaderVariable::GetInputSignatureElementDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/b36309e0-1c44-42d9-adcf-33acd753438c">Shader Structures</a>
 

 

