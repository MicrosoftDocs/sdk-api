---
UID: NF:d3d11.ID3D11DeviceContext.CSSetShader
title: ID3D11DeviceContext::CSSetShader (d3d11.h)
description: Set a compute shader to the device.
helpviewer_keywords: ["CSSetShader","CSSetShader method [Direct3D 11]","CSSetShader method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","CSSetShader method","ID3D11DeviceContext.CSSetShader","ID3D11DeviceContext::CSSetShader","cd24a33e-1a95-4033-49fc-875e68702c5b","d3d11/ID3D11DeviceContext::CSSetShader","direct3d11.id3d11devicecontext_cssetshader"]
old-location: direct3d11\id3d11devicecontext_cssetshader.htm
tech.root: direct3d11
ms.assetid: 97be7622-609f-4576-911a-93aa7f1b6b8c
ms.date: 12/05/2018
ms.keywords: CSSetShader, CSSetShader method [Direct3D 11], CSSetShader method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CSSetShader method, ID3D11DeviceContext.CSSetShader, ID3D11DeviceContext::CSSetShader, cd24a33e-1a95-4033-49fc-875e68702c5b, d3d11/ID3D11DeviceContext::CSSetShader, direct3d11.id3d11devicecontext_cssetshader
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
 - ID3D11DeviceContext::CSSetShader
 - d3d11/ID3D11DeviceContext::CSSetShader
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
 - ID3D11DeviceContext.CSSetShader
---

# ID3D11DeviceContext::CSSetShader


## -description

Set a compute shader to the device.

## -parameters

### -param pComputeShader [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader">ID3D11ComputeShader</a>*</b>

Pointer to a compute shader (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader">ID3D11ComputeShader</a>). Passing in <b>NULL</b> disables the shader for this pipeline stage.

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