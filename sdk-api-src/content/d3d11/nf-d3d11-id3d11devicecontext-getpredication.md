---
UID: NF:d3d11.ID3D11DeviceContext.GetPredication
title: ID3D11DeviceContext::GetPredication (d3d11.h)
description: Get the rendering predicate state. (ID3D11DeviceContext.GetPredication)
helpviewer_keywords: ["GetPredication","GetPredication method [Direct3D 11]","GetPredication method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","GetPredication method","ID3D11DeviceContext.GetPredication","ID3D11DeviceContext::GetPredication","ae323354-9c3a-634f-4e86-882e408d29d5","d3d11/ID3D11DeviceContext::GetPredication","direct3d11.id3d11devicecontext_getpredication"]
old-location: direct3d11\id3d11devicecontext_getpredication.htm
tech.root: direct3d11
ms.assetid: 9a283895-51c4-4de5-bdeb-994f3085bd79
ms.date: 12/05/2018
ms.keywords: GetPredication, GetPredication method [Direct3D 11], GetPredication method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],GetPredication method, ID3D11DeviceContext.GetPredication, ID3D11DeviceContext::GetPredication, ae323354-9c3a-634f-4e86-882e408d29d5, d3d11/ID3D11DeviceContext::GetPredication, direct3d11.id3d11devicecontext_getpredication
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
 - ID3D11DeviceContext::GetPredication
 - d3d11/ID3D11DeviceContext::GetPredication
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
 - ID3D11DeviceContext.GetPredication
---

# ID3D11DeviceContext::GetPredication


## -description

Get the rendering predicate state.

## -parameters

### -param ppPredicate [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate">ID3D11Predicate</a>**</b>

Address of a pointer to a predicate (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate">ID3D11Predicate</a>). Value stored here will be <b>NULL</b> upon device creation.

### -param pPredicateValue [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Address of a boolean to fill with the predicate comparison value. <b>FALSE</b> upon device creation.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
