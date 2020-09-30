---
UID: NF:d3d11.ID3D11DeviceContext.DSSetShader
title: ID3D11DeviceContext::DSSetShader (d3d11.h)
description: Set a domain shader to the device.
helpviewer_keywords: ["DSSetShader","DSSetShader method [Direct3D 11]","DSSetShader method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","DSSetShader method","ID3D11DeviceContext.DSSetShader","ID3D11DeviceContext::DSSetShader","b38d5392-9654-20ac-d78c-5d92274289d3","d3d11/ID3D11DeviceContext::DSSetShader","direct3d11.id3d11devicecontext_dssetshader"]
old-location: direct3d11\id3d11devicecontext_dssetshader.htm
tech.root: direct3d11
ms.assetid: 5ee4a072-3b4a-44e6-ae70-19e0888905a2
ms.date: 12/05/2018
ms.keywords: DSSetShader, DSSetShader method [Direct3D 11], DSSetShader method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DSSetShader method, ID3D11DeviceContext.DSSetShader, ID3D11DeviceContext::DSSetShader, b38d5392-9654-20ac-d78c-5d92274289d3, d3d11/ID3D11DeviceContext::DSSetShader, direct3d11.id3d11devicecontext_dssetshader
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
 - ID3D11DeviceContext::DSSetShader
 - d3d11/ID3D11DeviceContext::DSSetShader
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
 - ID3D11DeviceContext.DSSetShader
---

# ID3D11DeviceContext::DSSetShader


## -description

Set a domain shader to the device.

## -parameters

### -param pDomainShader [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader">ID3D11DomainShader</a>*</b>

Pointer to a domain shader (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader">ID3D11DomainShader</a>). Passing in <b>NULL</b> disables the shader for this pipeline stage.

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

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>