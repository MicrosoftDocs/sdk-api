---
UID: NF:d3d11.ID3D11DeviceContext.VSGetShader
title: ID3D11DeviceContext::VSGetShader (d3d11.h)
description: Get the vertex shader currently set on the device. (ID3D11DeviceContext.VSGetShader)
helpviewer_keywords: ["3e9ed365-9e14-baae-7c23-80439c5771f7","ID3D11DeviceContext interface [Direct3D 11]","VSGetShader method","ID3D11DeviceContext.VSGetShader","ID3D11DeviceContext::VSGetShader","VSGetShader","VSGetShader method [Direct3D 11]","VSGetShader method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::VSGetShader","direct3d11.id3d11devicecontext_vsgetshader"]
old-location: direct3d11\id3d11devicecontext_vsgetshader.htm
tech.root: direct3d11
ms.assetid: 03347303-bab2-46aa-81e8-7df75911ff21
ms.date: 12/05/2018
ms.keywords: 3e9ed365-9e14-baae-7c23-80439c5771f7, ID3D11DeviceContext interface [Direct3D 11],VSGetShader method, ID3D11DeviceContext.VSGetShader, ID3D11DeviceContext::VSGetShader, VSGetShader, VSGetShader method [Direct3D 11], VSGetShader method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::VSGetShader, direct3d11.id3d11devicecontext_vsgetshader
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
 - ID3D11DeviceContext::VSGetShader
 - d3d11/ID3D11DeviceContext::VSGetShader
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
 - ID3D11DeviceContext.VSGetShader
---

# ID3D11DeviceContext::VSGetShader


## -description

Get the vertex shader currently set on the device.

## -parameters

### -param ppVertexShader [out]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader">ID3D11VertexShader</a>**</b>

Address of a pointer to a vertex shader (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader">ID3D11VertexShader</a>) to be returned by the method.

### -param ppClassInstances [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>**</b>

Pointer to an array of class instance interfaces (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>).

### -param pNumClassInstances [in, out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

The number of class-instance elements in the array.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
