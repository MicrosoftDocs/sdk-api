---
UID: NF:d3d11.ID3D11Device.CreateQuery
title: ID3D11Device::CreateQuery (d3d11.h)
description: This interface encapsulates methods for querying information from the GPU. (ID3D11Device.CreateQuery)
helpviewer_keywords: ["CreateQuery","CreateQuery method [Direct3D 11]","CreateQuery method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreateQuery method","ID3D11Device.CreateQuery","ID3D11Device::CreateQuery","d3d11/ID3D11Device::CreateQuery","direct3d11.id3d11device_createquery","f2e88fab-8ad2-a5e2-0d8a-4c97538eb108"]
old-location: direct3d11\id3d11device_createquery.htm
tech.root: direct3d11
ms.assetid: ad09a309-862f-462d-8268-62e44397c298
ms.date: 12/05/2018
ms.keywords: CreateQuery, CreateQuery method [Direct3D 11], CreateQuery method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateQuery method, ID3D11Device.CreateQuery, ID3D11Device::CreateQuery, d3d11/ID3D11Device::CreateQuery, direct3d11.id3d11device_createquery, f2e88fab-8ad2-a5e2-0d8a-4c97538eb108
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
 - ID3D11Device::CreateQuery
 - d3d11/ID3D11Device::CreateQuery
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
 - ID3D11Device.CreateQuery
---

# ID3D11Device::CreateQuery


## -description

This interface encapsulates methods for querying information from the GPU.

## -parameters

### -param pQueryDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_query_desc">D3D11_QUERY_DESC</a>*</b>

Pointer to a query description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_query_desc">D3D11_QUERY_DESC</a>).

### -param ppQuery [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11query">ID3D11Query</a>**</b>

Address of a pointer to the query object created (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11query">ID3D11Query</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns E_OUTOFMEMORY if there is insufficient memory to create the query object.  
        See <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a> for other possible return values.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
