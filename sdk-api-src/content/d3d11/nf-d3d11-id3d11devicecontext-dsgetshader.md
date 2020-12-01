---
UID: NF:d3d11.ID3D11DeviceContext.DSGetShader
title: ID3D11DeviceContext::DSGetShader (d3d11.h)
description: Get the domain shader currently set on the device.
helpviewer_keywords: ["23ad23d5-5ea9-e2f1-ce64-770b35bc0586","DSGetShader","DSGetShader method [Direct3D 11]","DSGetShader method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","DSGetShader method","ID3D11DeviceContext.DSGetShader","ID3D11DeviceContext::DSGetShader","d3d11/ID3D11DeviceContext::DSGetShader","direct3d11.id3d11devicecontext_dsgetshader"]
old-location: direct3d11\id3d11devicecontext_dsgetshader.htm
tech.root: direct3d11
ms.assetid: b04a9640-e28e-419e-9a8c-02685e7a0883
ms.date: 12/05/2018
ms.keywords: 23ad23d5-5ea9-e2f1-ce64-770b35bc0586, DSGetShader, DSGetShader method [Direct3D 11], DSGetShader method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DSGetShader method, ID3D11DeviceContext.DSGetShader, ID3D11DeviceContext::DSGetShader, d3d11/ID3D11DeviceContext::DSGetShader, direct3d11.id3d11devicecontext_dsgetshader
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
 - ID3D11DeviceContext::DSGetShader
 - d3d11/ID3D11DeviceContext::DSGetShader
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
 - ID3D11DeviceContext.DSGetShader
---

# ID3D11DeviceContext::DSGetShader


## -description

Get the domain shader currently set on the device.

## -parameters

### -param ppDomainShader [out]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader">ID3D11DomainShader</a>**</b>

Address of a pointer to a domain shader (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader">ID3D11DomainShader</a>) to be returned by the method.

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