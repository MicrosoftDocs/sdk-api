---
UID: NF:d3d11shader.ID3D11ShaderReflectionVariable.GetDesc
title: ID3D11ShaderReflectionVariable::GetDesc
author: windows-sdk-content
description: Get a shader-variable description.
old-location: direct3d11\id3d11shaderreflectionvariable_getdesc.htm
tech.root: direct3d11
ms.assetid: a384e172-763f-4f4c-b6fb-f657fa31e5ee
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 6ae72773-659b-8911-13a0-cbaa49ed3c83, GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11ShaderReflectionVariable interface, ID3D11ShaderReflectionVariable interface [Direct3D 11],GetDesc method, ID3D11ShaderReflectionVariable.GetDesc, ID3D11ShaderReflectionVariable::GetDesc, d3d11shader/ID3D11ShaderReflectionVariable::GetDesc, direct3d11.id3d11shaderreflectionvariable_getdesc
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
 - ID3D11ShaderReflectionVariable.GetDesc
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
- ID3D11ShaderReflectionVariable.GetDesc
: 
---

# ID3D11ShaderReflectionVariable::GetDesc


## -description


Get a shader-variable description.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/b5620fea-c7d1-4db1-9bd1-991a2efa3b4c">D3D11_SHADER_VARIABLE_DESC</a>*</b>

A pointer to a shader-variable description (see <a href="https://msdn.microsoft.com/b5620fea-c7d1-4db1-9bd1-991a2efa3b4c">D3D11_SHADER_VARIABLE_DESC</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



This method can be used to determine if the <a href="https://msdn.microsoft.com/4422a51f-b190-4df0-a1bb-a8ee2cc66da2">ID3D11ShaderReflectionVariable Interface</a> is valid, the method returns <b>E_FAIL</b> when the variable is not valid.

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/4422a51f-b190-4df0-a1bb-a8ee2cc66da2">ID3D11ShaderReflectionVariable Interface</a>
 

 

