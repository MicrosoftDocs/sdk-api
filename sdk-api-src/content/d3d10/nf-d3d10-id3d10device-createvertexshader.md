---
UID: NF:d3d10.ID3D10Device.CreateVertexShader
title: ID3D10Device::CreateVertexShader (d3d10.h)
description: Create a vertex-shader object from a compiled shader. (ID3D10Device.CreateVertexShader)
helpviewer_keywords: ["85865e55-ec77-0246-1f72-283d1333b4e7","CreateVertexShader","CreateVertexShader method [Direct3D 10]","CreateVertexShader method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","CreateVertexShader method","ID3D10Device.CreateVertexShader","ID3D10Device::CreateVertexShader","d3d10/ID3D10Device::CreateVertexShader","direct3d10.id3d10device_createvertexshader"]
old-location: direct3d10\id3d10device_createvertexshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createvertexshader.htm
ms.date: 12/05/2018
ms.keywords: 85865e55-ec77-0246-1f72-283d1333b4e7, CreateVertexShader, CreateVertexShader method [Direct3D 10], CreateVertexShader method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateVertexShader method, ID3D10Device.CreateVertexShader, ID3D10Device::CreateVertexShader, d3d10/ID3D10Device::CreateVertexShader, direct3d10.id3d10device_createvertexshader
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::CreateVertexShader
 - d3d10/ID3D10Device::CreateVertexShader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CreateVertexShader
---

# ID3D10Device::CreateVertexShader


## -description

Create a vertex-shader object from a compiled shader.

## -parameters

### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader. To get this pointer see <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10">Getting a Pointer to a Compiled Shader</a>.

### -param BytecodeLength [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Size of the compiled vertex shader.

### -param ppVertexShader [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10vertexshader">ID3D10VertexShader</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10vertexshader">ID3D10VertexShader Interface</a>. If this is <b>NULL</b>, all other parameters will be validated, and if all parameters pass validation this API will return S_FALSE instead of S_OK.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
