---
UID: NF:d3d11.ID3D11DeviceContext.CSGetShader
title: ID3D11DeviceContext::CSGetShader (d3d11.h)
description: Get the compute shader currently set on the device.
helpviewer_keywords: ["CSGetShader","CSGetShader method [Direct3D 11]","CSGetShader method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","CSGetShader method","ID3D11DeviceContext.CSGetShader","ID3D11DeviceContext::CSGetShader","d3d11/ID3D11DeviceContext::CSGetShader","d55a8dcd-a09c-0388-1870-f4bcb519d6b1","direct3d11.id3d11devicecontext_csgetshader"]
old-location: direct3d11\id3d11devicecontext_csgetshader.htm
tech.root: direct3d11
ms.assetid: ddd09ca8-ab1f-4d1d-a182-44e48bac93c5
ms.date: 12/05/2018
ms.keywords: CSGetShader, CSGetShader method [Direct3D 11], CSGetShader method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CSGetShader method, ID3D11DeviceContext.CSGetShader, ID3D11DeviceContext::CSGetShader, d3d11/ID3D11DeviceContext::CSGetShader, d55a8dcd-a09c-0388-1870-f4bcb519d6b1, direct3d11.id3d11devicecontext_csgetshader
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
 - ID3D11DeviceContext::CSGetShader
 - d3d11/ID3D11DeviceContext::CSGetShader
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
 - ID3D11DeviceContext.CSGetShader
---

# ID3D11DeviceContext::CSGetShader


## -description

Get the compute shader currently set on the device.

## -parameters

### -param ppComputeShader [out]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader">ID3D11ComputeShader</a>**</b>

Address of a pointer to a Compute shader (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader">ID3D11ComputeShader</a>) to be returned by the method.

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