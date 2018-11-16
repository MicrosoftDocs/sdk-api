---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetPatchConstantParameterDesc
title: ID3D11ShaderReflection::GetPatchConstantParameterDesc
author: windows-sdk-content
description: Get a patch-constant parameter description for a shader.
old-location: direct3d11\id3d11shaderreflection_getpatchconstantparameterdesc.htm
tech.root: direct3d11
ms.assetid: 91a1a3ac-1dd4-4d91-aaea-196a99d5d684
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetPatchConstantParameterDesc, GetPatchConstantParameterDesc method [Direct3D 11], GetPatchConstantParameterDesc method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetPatchConstantParameterDesc method, ID3D11ShaderReflection.GetPatchConstantParameterDesc, ID3D11ShaderReflection::GetPatchConstantParameterDesc, a1d3c039-54af-ae32-0c02-c7d90751aacc, d3d11shader/ID3D11ShaderReflection::GetPatchConstantParameterDesc, direct3d11.id3d11shaderreflection_getpatchconstantparameterdesc
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
 - ID3D11ShaderReflection.GetPatchConstantParameterDesc
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
- ID3D11ShaderReflection.GetPatchConstantParameterDesc
: 
---

# ID3D11ShaderReflection::GetPatchConstantParameterDesc


## -description


Get a patch-constant parameter description for a shader.


## -parameters




### -param ParameterIndex [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

A zero-based parameter index.


### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476215(v=VS.85).aspx">D3D11_SIGNATURE_PARAMETER_DESC</a>*</b>

A pointer to a shader-input-signature description. See <a href="https://msdn.microsoft.com/en-us/library/Ff476215(v=VS.85).aspx">D3D11_SIGNATURE_PARAMETER_DESC</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.




## -remarks



This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476590(v=VS.85).aspx">ID3D11ShaderReflection Interface</a>
 

 

