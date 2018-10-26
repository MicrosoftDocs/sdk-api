---
UID: NS:d3d11shader._D3D11_SIGNATURE_PARAMETER_DESC
title: "_D3D11_SIGNATURE_PARAMETER_DESC"
author: windows-sdk-content
description: Describes a shader signature.
old-location: direct3d11\d3d11_signature_parameter_desc.htm
tech.root: direct3d11
ms.assetid: 3aed2f5f-1cfa-4224-bfcc-7d015e6a2cc0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D11_SIGNATURE_PARAMETER_DESC, D3D11_SIGNATURE_PARAMETER_DESC structure [Direct3D 11], _D3D11_SIGNATURE_PARAMETER_DESC, d3d11shader/D3D11_SIGNATURE_PARAMETER_DESC, direct3d11.d3d11_signature_parameter_desc, e870121a-ce22-1699-8203-c018e7d5db8e
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11Shader.h
api_name:
 - D3D11_SIGNATURE_PARAMETER_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_SIGNATURE_PARAMETER_DESC
req.redist: 
---

# _D3D11_SIGNATURE_PARAMETER_DESC structure


## -description


Describes a shader signature.


## -struct-fields




### -field SemanticName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

A per-parameter string that identifies how the data will be used. For more info, see <a href="https://msdn.microsoft.com/6f5c504c-1940-4d1c-b594-a2132599376b">Semantics</a>. 


### -field SemanticIndex

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Semantic index that modifies the semantic. Used to differentiate different parameters that use the same semantic.


### -field Register

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The register that will contain this variable's data.


### -field SystemValueType

Type: <b><a href="https://msdn.microsoft.com/16675331-36cf-4086-a753-6d80ee934ace">D3D_NAME</a></b>

A <a href="https://msdn.microsoft.com/16675331-36cf-4086-a753-6d80ee934ace">D3D_NAME</a>-typed value that identifies a predefined string that determines the functionality of certain pipeline stages.


### -field ComponentType

Type: <b><a href="https://msdn.microsoft.com/71e3c707-745b-40b4-ba3c-6c501196e3d3">D3D_REGISTER_COMPONENT_TYPE</a></b>

A <a href="https://msdn.microsoft.com/71e3c707-745b-40b4-ba3c-6c501196e3d3">D3D_REGISTER_COMPONENT_TYPE</a>-typed value that identifies the per-component-data type that is stored in a register.  Each register can store up to four-components of data.


### -field Mask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Mask which indicates which components of a register are used.


### -field ReadWriteMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Mask which indicates whether a given component is never written (if the signature is an output signature) or always read (if the signature is an input signature). 


### -field Stream

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Indicates which stream the geometry shader is using for the signature parameter.


### -field MinPrecision

Type: <b><a href="https://msdn.microsoft.com/C97D04D7-EAE4-4E5B-80A2-EDB1CE68C2BC">D3D_MIN_PRECISION</a></b>

A <a href="https://msdn.microsoft.com/C97D04D7-EAE4-4E5B-80A2-EDB1CE68C2BC">D3D_MIN_PRECISION</a>-typed value that indicates the minimum desired interpolation precision. For more info, see <a href="https://msdn.microsoft.com/422B0C45-5CEB-4235-AD05-62D36C36CFC6">Using HLSL minimum precision</a>.


## -remarks



A shader can take n inputs and can produce m outputs. The order of the input (or output) parameters, their associated types, and any attached semantics make up the shader signature. Each shader has an input and an output signature.

When compiling a shader or an effect, some API calls validate shader signatures  That is, they compare the output signature of one shader (like a vertex shader) with the input signature of another shader (like a pixel shader). This ensures that a shader outputs data that is compatible with a downstream shader that is consuming that data. Compatible means that a shader signature is a exact-match subset of the preceding shader stage. Exact match means parameter types and semantics must exactly match. Subset means that a parameter that is not required by a downstream stage, does not need to include that parameter in its shader signature.

Get a shader-signature from a shader or an effect by calling APIs such as <a href="https://msdn.microsoft.com/6483634d-6050-4218-98ee-a7062efcbe64">ID3D11ShaderReflection::GetInputParameterDesc</a>. 




## -see-also




<a href="https://msdn.microsoft.com/3b8ece5c-5065-4711-b12c-06cf7ea0e1ba">Shader Structures</a>
 

 

