---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetInputParameterDesc
title: ID3D11ShaderReflection::GetInputParameterDesc
author: windows-sdk-content
description: Get an input-parameter description for a shader.
old-location: direct3d11\id3d11shaderreflection_getinputparameterdesc.htm
tech.root: direct3d11
ms.assetid: 6483634d-6050-4218-98ee-a7062efcbe64
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 06783a52-4fd2-1c86-8b0d-40efb3e6ac1e, GetInputParameterDesc, GetInputParameterDesc method [Direct3D 11], GetInputParameterDesc method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetInputParameterDesc method, ID3D11ShaderReflection.GetInputParameterDesc, ID3D11ShaderReflection::GetInputParameterDesc, d3d11shader/ID3D11ShaderReflection::GetInputParameterDesc, direct3d11.id3d11shaderreflection_getinputparameterdesc
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
 - ID3D11ShaderReflection.GetInputParameterDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11shader.h
: 
- ID3D11ShaderReflection.GetInputParameterDesc
: 
---

# ID3D11ShaderReflection::GetInputParameterDesc


## -description


Get an input-parameter description for a shader.


## -parameters




### -param ParameterIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based parameter index.


### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/3aed2f5f-1cfa-4224-bfcc-7d015e6a2cc0">D3D11_SIGNATURE_PARAMETER_DESC</a>*</b>

A pointer to a shader-input-signature description. See <a href="https://msdn.microsoft.com/3aed2f5f-1cfa-4224-bfcc-7d015e6a2cc0">D3D11_SIGNATURE_PARAMETER_DESC</a>.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -remarks



An input-parameter description is also called a shader signature. The shader signature contains information about the input parameters such as the order or parameters, their data type, and a parameter semantic.

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/a28cca72-7f2d-416a-bfa9-4d1f71fc98d5">ID3D11ShaderReflection Interface</a>
 

 

