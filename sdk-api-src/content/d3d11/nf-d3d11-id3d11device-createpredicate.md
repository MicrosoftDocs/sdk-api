---
UID: NF:d3d11.ID3D11Device.CreatePredicate
title: ID3D11Device::CreatePredicate (d3d11.h)
description: Creates a predicate. (ID3D11Device.CreatePredicate)
helpviewer_keywords: ["3892a0ec-dd05-6f9e-18d3-d6cc2cc95d5f","CreatePredicate","CreatePredicate method [Direct3D 11]","CreatePredicate method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreatePredicate method","ID3D11Device.CreatePredicate","ID3D11Device::CreatePredicate","d3d11/ID3D11Device::CreatePredicate","direct3d11.id3d11device_createpredicate"]
old-location: direct3d11\id3d11device_createpredicate.htm
tech.root: direct3d11
ms.assetid: 5af4e63b-ba85-4c73-82e3-b09579d7ce78
ms.date: 12/05/2018
ms.keywords: 3892a0ec-dd05-6f9e-18d3-d6cc2cc95d5f, CreatePredicate, CreatePredicate method [Direct3D 11], CreatePredicate method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreatePredicate method, ID3D11Device.CreatePredicate, ID3D11Device::CreatePredicate, d3d11/ID3D11Device::CreatePredicate, direct3d11.id3d11device_createpredicate
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
 - ID3D11Device::CreatePredicate
 - d3d11/ID3D11Device::CreatePredicate
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
 - ID3D11Device.CreatePredicate
---

# ID3D11Device::CreatePredicate


## -description

Creates a predicate.

## -parameters

### -param pPredicateDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_query_desc">D3D11_QUERY_DESC</a>*</b>

Pointer to a query description where the type of query must be a D3D11_QUERY_SO_OVERFLOW_PREDICATE or D3D11_QUERY_OCCLUSION_PREDICATE (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_query_desc">D3D11_QUERY_DESC</a>).

### -param ppPredicate [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate">ID3D11Predicate</a>**</b>

Address of a pointer to a predicate (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate">ID3D11Predicate</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
