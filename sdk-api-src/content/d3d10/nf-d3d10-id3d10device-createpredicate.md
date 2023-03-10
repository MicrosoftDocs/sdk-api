---
UID: NF:d3d10.ID3D10Device.CreatePredicate
title: ID3D10Device::CreatePredicate (d3d10.h)
description: Creates a predicate. (ID3D10Device.CreatePredicate)
helpviewer_keywords: ["2b30a615-97cf-d010-fc84-3802da398aee","CreatePredicate","CreatePredicate method [Direct3D 10]","CreatePredicate method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","CreatePredicate method","ID3D10Device.CreatePredicate","ID3D10Device::CreatePredicate","d3d10/ID3D10Device::CreatePredicate","direct3d10.id3d10device_createpredicate"]
old-location: direct3d10\id3d10device_createpredicate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createpredicate.htm
ms.date: 12/05/2018
ms.keywords: 2b30a615-97cf-d010-fc84-3802da398aee, CreatePredicate, CreatePredicate method [Direct3D 10], CreatePredicate method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreatePredicate method, ID3D10Device.CreatePredicate, ID3D10Device::CreatePredicate, d3d10/ID3D10Device::CreatePredicate, direct3d10.id3d10device_createpredicate
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::CreatePredicate
 - d3d10/ID3D10Device::CreatePredicate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CreatePredicate
---

# ID3D10Device::CreatePredicate


## -description

Creates a predicate.

## -parameters

### -param pPredicateDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_query_desc">D3D10_QUERY_DESC</a>*</b>

Pointer to a query description where the type of query must be a D3D10_QUERY_SO_OVERFLOW_PREDICATE or D3D10_QUERY_OCCLUSION_PREDICATE (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_query_desc">D3D10_QUERY_DESC</a>).

### -param ppPredicate [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10predicate">ID3D10Predicate</a>**</b>

Address of a pointer to a predicate (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10predicate">ID3D10Predicate Interface</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
