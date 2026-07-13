---
UID: NF:d3d11shader.ID3D11ShaderReflectionConstantBuffer.GetDesc
title: ID3D11ShaderReflectionConstantBuffer::GetDesc (d3d11shader.h)
description: Get a constant-buffer description. (ID3D11ShaderReflectionConstantBuffer.GetDesc)
helpviewer_keywords: ["3b59f7a3-fb44-16a7-ef26-3f7e3b33ec7b","GetDesc","GetDesc method [Direct3D 11]","GetDesc method [Direct3D 11]","ID3D11ShaderReflectionConstantBuffer interface","ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11]","GetDesc method","ID3D11ShaderReflectionConstantBuffer.GetDesc","ID3D11ShaderReflectionConstantBuffer::GetDesc","d3d11shader/ID3D11ShaderReflectionConstantBuffer::GetDesc","direct3d11.id3d11shaderreflectionconstantbuffer_getdesc"]
old-location: direct3d11\id3d11shaderreflectionconstantbuffer_getdesc.htm
tech.root: direct3d11
ms.assetid: 34d84751-ccce-4c18-8027-2b5477e35abc
ms.date: 12/05/2018
ms.keywords: 3b59f7a3-fb44-16a7-ef26-3f7e3b33ec7b, GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11ShaderReflectionConstantBuffer interface, ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11],GetDesc method, ID3D11ShaderReflectionConstantBuffer.GetDesc, ID3D11ShaderReflectionConstantBuffer::GetDesc, d3d11shader/ID3D11ShaderReflectionConstantBuffer::GetDesc, direct3d11.id3d11shaderreflectionconstantbuffer_getdesc
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ShaderReflectionConstantBuffer::GetDesc
 - d3d11shader/ID3D11ShaderReflectionConstantBuffer::GetDesc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11ShaderReflectionConstantBuffer.GetDesc
---

# ID3D11ShaderReflectionConstantBuffer::GetDesc


## -description

Get a constant-buffer description.

## -parameters

### -param pDesc

Type: <b><a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_buffer_desc">D3D11_SHADER_BUFFER_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_buffer_desc">D3D11_SHADER_BUFFER_DESC</a>, which represents a shader-buffer description.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer">ID3D11ShaderReflectionConstantBuffer Interface</a>
