---
UID: NF:d3d11shader.ID3D11ShaderReflectionConstantBuffer.GetVariableByIndex
title: ID3D11ShaderReflectionConstantBuffer::GetVariableByIndex (d3d11shader.h)
author: windows-sdk-content
description: Get a shader-reflection variable by index.
old-location: direct3d11\id3d11shaderreflectionconstantbuffer_getvariablebyindex.htm
tech.root: direct3d11
ms.assetid: fafdf040-223c-4e69-95b6-05c62ea8ff52
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 45c0f056-8446-d61d-24b8-31ff2f2a92ff, GetVariableByIndex, GetVariableByIndex method [Direct3D 11], GetVariableByIndex method [Direct3D 11],ID3D11ShaderReflectionConstantBuffer interface, ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11],GetVariableByIndex method, ID3D11ShaderReflectionConstantBuffer.GetVariableByIndex, ID3D11ShaderReflectionConstantBuffer::GetVariableByIndex, d3d11shader/ID3D11ShaderReflectionConstantBuffer::GetVariableByIndex, direct3d11.id3d11shaderreflectionconstantbuffer_getvariablebyindex
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
 - ID3D11ShaderReflectionConstantBuffer.GetVariableByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11ShaderReflectionConstantBuffer::GetVariableByIndex


## -description


Get a shader-reflection variable by index.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Zero-based index.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4422a51f-b190-4df0-a1bb-a8ee2cc66da2">ID3D11ShaderReflectionVariable</a>*</b>

A pointer to a shader-reflection variable interface (see <a href="https://msdn.microsoft.com/4422a51f-b190-4df0-a1bb-a8ee2cc66da2">ID3D11ShaderReflectionVariable Interface</a>).




## -remarks



This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/4b47ed8d-e814-4a7b-bc8e-25a8b71200ce">ID3D11ShaderReflectionConstantBuffer Interface</a>
 

 

