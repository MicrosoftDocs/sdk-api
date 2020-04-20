---
UID: NF:d3d10shader.ID3D10ShaderReflection.GetConstantBufferByIndex
title: ID3D10ShaderReflection::GetConstantBufferByIndex (d3d10shader.h)
description: Get a constant buffer by index.helpviewer_keywords: ["GetConstantBufferByIndex","GetConstantBufferByIndex method [Direct3D 10]","GetConstantBufferByIndex method [Direct3D 10]","ID3D10ShaderReflection interface","ID3D10ShaderReflection interface [Direct3D 10]","GetConstantBufferByIndex method","ID3D10ShaderReflection.GetConstantBufferByIndex","ID3D10ShaderReflection::GetConstantBufferByIndex","d3d10shader/ID3D10ShaderReflection::GetConstantBufferByIndex","df0b7d8a-d6eb-ab55-7076-d5723df0ee5d","direct3d10.id3d10shaderreflection_getconstantbufferbyindex"]
old-location: direct3d10\id3d10shaderreflection_getconstantbufferbyindex.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection_getconstantbufferbyindex.htm
ms.date: 12/05/2018
ms.keywords: GetConstantBufferByIndex, GetConstantBufferByIndex method [Direct3D 10], GetConstantBufferByIndex method [Direct3D 10],ID3D10ShaderReflection interface, ID3D10ShaderReflection interface [Direct3D 10],GetConstantBufferByIndex method, ID3D10ShaderReflection.GetConstantBufferByIndex, ID3D10ShaderReflection::GetConstantBufferByIndex, d3d10shader/ID3D10ShaderReflection::GetConstantBufferByIndex, df0b7d8a-d6eb-ab55-7076-d5723df0ee5d, direct3d10.id3d10shaderreflection_getconstantbufferbyindex
ms.topic: method
f1_keywords:
- d3d10shader/ID3D10ShaderReflection.GetConstantBufferByIndex
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D10Shader.h
api_name:
- ID3D10ShaderReflection.GetConstantBufferByIndex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10ShaderReflection::GetConstantBufferByIndex


## -description


Get a constant buffer by index.


## -parameters




### -param Index [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based index.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer">ID3D10ShaderReflectionConstantBuffer</a>*</b>

A pointer to a constant buffer (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer">ID3D10ShaderReflectionConstantBuffer Interface</a>).




## -remarks



A constant buffer supplies either scalar constants or texture constants to a shader. A shader can use one or more constant buffers. For best performance, separate constants into buffers based on the frequency they are updated.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection">ID3D10ShaderReflection Interface</a>
 

 

