---
UID: NF:d3d11.ID3D11Device.CreateClassLinkage
title: ID3D11Device::CreateClassLinkage (d3d11.h)
description: Creates class linkage libraries to enable dynamic shader linkage.
helpviewer_keywords: ["411c8228-de78-2b45-6754-17ebcd3ef8de","CreateClassLinkage","CreateClassLinkage method [Direct3D 11]","CreateClassLinkage method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreateClassLinkage method","ID3D11Device.CreateClassLinkage","ID3D11Device::CreateClassLinkage","d3d11/ID3D11Device::CreateClassLinkage","direct3d11.id3d11device_createclasslinkage"]
old-location: direct3d11\id3d11device_createclasslinkage.htm
tech.root: direct3d11
ms.assetid: 1d68e977-bcdc-4aab-9434-29200553a69e
ms.date: 12/05/2018
ms.keywords: 411c8228-de78-2b45-6754-17ebcd3ef8de, CreateClassLinkage, CreateClassLinkage method [Direct3D 11], CreateClassLinkage method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateClassLinkage method, ID3D11Device.CreateClassLinkage, ID3D11Device::CreateClassLinkage, d3d11/ID3D11Device::CreateClassLinkage, direct3d11.id3d11device_createclasslinkage
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
 - ID3D11Device::CreateClassLinkage
 - d3d11/ID3D11Device::CreateClassLinkage
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
 - ID3D11Device.CreateClassLinkage
---

# ID3D11Device::CreateClassLinkage


## -description

Creates class linkage libraries to enable dynamic shader linkage.

## -parameters

### -param ppLinkage [out]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a>**</b>

A pointer to a class-linkage interface pointer (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

The <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a> interface returned in <i>ppLinkage</i> is associated with a shader by passing it as a parameter to one of the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> create shader methods such as <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader">ID3D11Device::CreatePixelShader</a>.


#### Examples

Using CreateClassLinkage
          


```

ID3D11ClassLinkage * g_pPSClassLinkage = NULL;            
pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage ); 
          
```


<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>