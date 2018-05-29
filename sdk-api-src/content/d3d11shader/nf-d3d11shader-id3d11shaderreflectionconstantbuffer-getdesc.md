---
UID: NF:d3d11shader.ID3D11ShaderReflectionConstantBuffer.GetDesc
title: ID3D11ShaderReflectionConstantBuffer::GetDesc
author: windows-sdk-content
description: Get a constant-buffer description.
old-location: direct3d11\id3d11shaderreflectionconstantbuffer_getdesc.htm
old-project: direct3d11
ms.assetid: 34d84751-ccce-4c18-8027-2b5477e35abc
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 3b59f7a3-fb44-16a7-ef26-3f7e3b33ec7b, GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11ShaderReflectionConstantBuffer interface, ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11],GetDesc method, ID3D11ShaderReflectionConstantBuffer.GetDesc, ID3D11ShaderReflectionConstantBuffer::GetDesc, d3d11shader/ID3D11ShaderReflectionConstantBuffer::GetDesc, direct3d11.id3d11shaderreflectionconstantbuffer_getdesc
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
req.typenames: D3D11_SHADER_VERSION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3DCompiler_47.dll
api_name:
-	ID3D11ShaderReflectionConstantBuffer.GetDesc
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11ShaderReflectionConstantBuffer::GetDesc


## -description


Get a constant-buffer description.


## -parameters




### -param pDesc

Type: <b><a href="https://msdn.microsoft.com/deea8d5d-2431-4449-baa8-68a4b9b30307">D3D11_SHADER_BUFFER_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/deea8d5d-2431-4449-baa8-68a4b9b30307">D3D11_SHADER_BUFFER_DESC</a>, which represents a shader-buffer description.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/4b47ed8d-e814-4a7b-bc8e-25a8b71200ce">ID3D11ShaderReflectionConstantBuffer Interface</a>
 

 

