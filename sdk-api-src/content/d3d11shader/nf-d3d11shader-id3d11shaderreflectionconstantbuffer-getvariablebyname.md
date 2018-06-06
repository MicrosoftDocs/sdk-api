---
UID: NF:d3d11shader.ID3D11ShaderReflectionConstantBuffer.GetVariableByName
title: ID3D11ShaderReflectionConstantBuffer::GetVariableByName
author: windows-sdk-content
description: Get a shader-reflection variable by name.
old-location: direct3d11\id3d11shaderreflectionconstantbuffer_getvariablebyname.htm
old-project: direct3d11
ms.assetid: daa14557-0987-4498-a2f5-428497805eca
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 613cfca7-07e9-dcae-c494-e5cdf1002b8c, GetVariableByName, GetVariableByName method [Direct3D 11], GetVariableByName method [Direct3D 11],ID3D11ShaderReflectionConstantBuffer interface, ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11],GetVariableByName method, ID3D11ShaderReflectionConstantBuffer.GetVariableByName, ID3D11ShaderReflectionConstantBuffer::GetVariableByName, d3d11shader/ID3D11ShaderReflectionConstantBuffer::GetVariableByName, direct3d11.id3d11shaderreflectionconstantbuffer_getvariablebyname
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
 - ID3D11ShaderReflectionConstantBuffer.GetVariableByName
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11ShaderReflectionConstantBuffer::GetVariableByName


## -description


Get a shader-reflection variable by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

Variable name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4422a51f-b190-4df0-a1bb-a8ee2cc66da2">ID3D11ShaderReflectionVariable</a>*</b>

Returns a sentinel object (end of list marker). To determine if GetVariableByName successfully completed, call <a href="https://msdn.microsoft.com/a384e172-763f-4f4c-b6fb-f657fa31e5ee">ID3D11ShaderReflectionVariable::GetDesc</a> and check the returned <b>HRESULT</b>; any return value other than success means that GetVariableByName failed.




## -remarks



This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/4b47ed8d-e814-4a7b-bc8e-25a8b71200ce">ID3D11ShaderReflectionConstantBuffer Interface</a>
 

 

