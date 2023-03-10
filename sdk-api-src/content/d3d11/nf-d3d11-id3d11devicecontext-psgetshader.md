---
UID: NF:d3d11.ID3D11DeviceContext.PSGetShader
title: ID3D11DeviceContext::PSGetShader (d3d11.h)
description: Get the pixel shader currently set on the device. (ID3D11DeviceContext.PSGetShader)
helpviewer_keywords: ["670956b7-c83d-77ff-bc7b-f0c5ef8d9986","ID3D11DeviceContext interface [Direct3D 11]","PSGetShader method","ID3D11DeviceContext.PSGetShader","ID3D11DeviceContext::PSGetShader","PSGetShader","PSGetShader method [Direct3D 11]","PSGetShader method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::PSGetShader","direct3d11.id3d11devicecontext_psgetshader"]
old-location: direct3d11\id3d11devicecontext_psgetshader.htm
tech.root: direct3d11
ms.assetid: 6ebeb763-b517-468c-bd46-022a426e0b6e
ms.date: 12/05/2018
ms.keywords: 670956b7-c83d-77ff-bc7b-f0c5ef8d9986, ID3D11DeviceContext interface [Direct3D 11],PSGetShader method, ID3D11DeviceContext.PSGetShader, ID3D11DeviceContext::PSGetShader, PSGetShader, PSGetShader method [Direct3D 11], PSGetShader method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::PSGetShader, direct3d11.id3d11devicecontext_psgetshader
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
 - ID3D11DeviceContext::PSGetShader
 - d3d11/ID3D11DeviceContext::PSGetShader
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
 - ID3D11DeviceContext.PSGetShader
---

# ID3D11DeviceContext::PSGetShader


## -description

Get the pixel shader currently set on the device.

## -parameters

### -param ppPixelShader [out]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader">ID3D11PixelShader</a>**</b>

Address of a pointer to a pixel shader (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader">ID3D11PixelShader</a>) to be returned by the method.

### -param ppClassInstances [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>**</b>

Pointer to an array of class instance interfaces (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>).

### -param pNumClassInstances [in, out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

The number of class-instance elements in the array.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed, to avoid memory leaks.
        

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
