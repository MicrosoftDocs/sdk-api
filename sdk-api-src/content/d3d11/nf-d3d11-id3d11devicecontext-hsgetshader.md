---
UID: NF:d3d11.ID3D11DeviceContext.HSGetShader
title: ID3D11DeviceContext::HSGetShader (d3d11.h)
description: Get the hull shader currently set on the device.
helpviewer_keywords: ["86d0e4a8-a23d-ed0e-3574-68679ce095a8","HSGetShader","HSGetShader method [Direct3D 11]","HSGetShader method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","HSGetShader method","ID3D11DeviceContext.HSGetShader","ID3D11DeviceContext::HSGetShader","d3d11/ID3D11DeviceContext::HSGetShader","direct3d11.id3d11devicecontext_hsgetshader"]
old-location: direct3d11\id3d11devicecontext_hsgetshader.htm
tech.root: direct3d11
ms.assetid: 2ac2d88f-8c66-490e-add8-95ecaadf0147
ms.date: 12/05/2018
ms.keywords: 86d0e4a8-a23d-ed0e-3574-68679ce095a8, HSGetShader, HSGetShader method [Direct3D 11], HSGetShader method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],HSGetShader method, ID3D11DeviceContext.HSGetShader, ID3D11DeviceContext::HSGetShader, d3d11/ID3D11DeviceContext::HSGetShader, direct3d11.id3d11devicecontext_hsgetshader
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
 - ID3D11DeviceContext::HSGetShader
 - d3d11/ID3D11DeviceContext::HSGetShader
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
 - ID3D11DeviceContext.HSGetShader
---

# ID3D11DeviceContext::HSGetShader


## -description

Get the hull shader currently set on the device.

## -parameters

### -param ppHullShader [out]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader">ID3D11HullShader</a>**</b>

Address of a pointer to a hull shader (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader">ID3D11HullShader</a>) to be returned by the method.

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