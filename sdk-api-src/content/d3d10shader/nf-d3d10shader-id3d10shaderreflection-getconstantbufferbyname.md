---
UID: NF:d3d10shader.ID3D10ShaderReflection.GetConstantBufferByName
title: ID3D10ShaderReflection::GetConstantBufferByName (d3d10shader.h)
description: Get a constant buffer by name. (ID3D10ShaderReflection.GetConstantBufferByName)
helpviewer_keywords: ["GetConstantBufferByName","GetConstantBufferByName method [Direct3D 10]","GetConstantBufferByName method [Direct3D 10]","ID3D10ShaderReflection interface","ID3D10ShaderReflection interface [Direct3D 10]","GetConstantBufferByName method","ID3D10ShaderReflection.GetConstantBufferByName","ID3D10ShaderReflection::GetConstantBufferByName","c597f147-5514-438b-1e81-09771d342a5f","d3d10shader/ID3D10ShaderReflection::GetConstantBufferByName","direct3d10.id3d10shaderreflection_getconstantbufferbyname"]
old-location: direct3d10\id3d10shaderreflection_getconstantbufferbyname.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection_getconstantbufferbyname.htm
ms.date: 12/05/2018
ms.keywords: GetConstantBufferByName, GetConstantBufferByName method [Direct3D 10], GetConstantBufferByName method [Direct3D 10],ID3D10ShaderReflection interface, ID3D10ShaderReflection interface [Direct3D 10],GetConstantBufferByName method, ID3D10ShaderReflection.GetConstantBufferByName, ID3D10ShaderReflection::GetConstantBufferByName, c597f147-5514-438b-1e81-09771d342a5f, d3d10shader/ID3D10ShaderReflection::GetConstantBufferByName, direct3d10.id3d10shaderreflection_getconstantbufferbyname
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10ShaderReflection::GetConstantBufferByName
 - d3d10shader/ID3D10ShaderReflection::GetConstantBufferByName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Shader.h
api_name:
 - ID3D10ShaderReflection.GetConstantBufferByName
---

# ID3D10ShaderReflection::GetConstantBufferByName


## -description

Get a constant buffer by name.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The constant-buffer name.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer">ID3D10ShaderReflectionConstantBuffer</a>*</b>

A pointer to a constant buffer (see <a href="/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer">ID3D10ShaderReflectionConstantBuffer Interface</a>).

## -remarks

A constant buffer supplies either scalar constants or texture constants to a shader. A shader can use one or more constant buffers. For best performance, separate constants into buffers based on the frequency they are updated.

## -see-also

<a href="/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection">ID3D10ShaderReflection Interface</a>
