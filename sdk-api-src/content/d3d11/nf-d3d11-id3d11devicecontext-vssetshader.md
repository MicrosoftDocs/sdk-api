---
UID: NF:d3d11.ID3D11DeviceContext.VSSetShader
title: ID3D11DeviceContext::VSSetShader (d3d11.h)
description: Set a vertex shader to the device. (ID3D11DeviceContext.VSSetShader)
helpviewer_keywords: ["2642b72a-9d7a-0eff-a9a4-df4e0b8eca75","ID3D11DeviceContext interface [Direct3D 11]","VSSetShader method","ID3D11DeviceContext.VSSetShader","ID3D11DeviceContext::VSSetShader","VSSetShader","VSSetShader method [Direct3D 11]","VSSetShader method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::VSSetShader","direct3d11.id3d11devicecontext_vssetshader"]
old-location: direct3d11\id3d11devicecontext_vssetshader.htm
tech.root: direct3d11
ms.assetid: d6207779-7477-4e74-beb8-065949abce06
ms.date: 12/05/2018
ms.keywords: 2642b72a-9d7a-0eff-a9a4-df4e0b8eca75, ID3D11DeviceContext interface [Direct3D 11],VSSetShader method, ID3D11DeviceContext.VSSetShader, ID3D11DeviceContext::VSSetShader, VSSetShader, VSSetShader method [Direct3D 11], VSSetShader method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::VSSetShader, direct3d11.id3d11devicecontext_vssetshader
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::VSSetShader
 - d3d11/ID3D11DeviceContext::VSSetShader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.VSSetShader
---

# ID3D11DeviceContext::VSSetShader


## -description

Set a vertex shader to the device.

## -parameters

### -param pVertexShader [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader">ID3D11VertexShader</a>*</b>

Pointer to a vertex shader (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader">ID3D11VertexShader</a>). Passing in <b>NULL</b> disables the shader for this pipeline stage.

### -param ppClassInstances [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>*</b>

A pointer to an array of class-instance interfaces (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>). Each interface used by a shader must have a corresponding class instance or the shader will get disabled. Set ppClassInstances to <b>NULL</b> if the shader does not use any interfaces.

### -param NumClassInstances

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of class-instance interfaces in the array.

## -remarks

The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.

The maximum number of instances a shader can have is 256.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
