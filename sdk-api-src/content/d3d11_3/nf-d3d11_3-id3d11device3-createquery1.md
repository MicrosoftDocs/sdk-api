---
UID: NF:d3d11_3.ID3D11Device3.CreateQuery1
title: ID3D11Device3::CreateQuery1 (d3d11_3.h)
description: Creates a query object for querying information from the graphics processing unit (GPU).
helpviewer_keywords: ["CreateQuery1","CreateQuery1 method [Direct3D 11]","CreateQuery1 method [Direct3D 11]","ID3D11Device3 interface","ID3D11Device3 interface [Direct3D 11]","CreateQuery1 method","ID3D11Device3.CreateQuery1","ID3D11Device3::CreateQuery1","d3d11_3/ID3D11Device3::CreateQuery1","direct3d11.id3d11device3_createquery1"]
old-location: direct3d11\id3d11device3_createquery1.htm
tech.root: direct3d11
ms.assetid: 8D170F97-DA95-48FE-84F6-2BBB3E388BB4
ms.date: 12/05/2018
ms.keywords: CreateQuery1, CreateQuery1 method [Direct3D 11], CreateQuery1 method [Direct3D 11],ID3D11Device3 interface, ID3D11Device3 interface [Direct3D 11],CreateQuery1 method, ID3D11Device3.CreateQuery1, ID3D11Device3::CreateQuery1, d3d11_3/ID3D11Device3::CreateQuery1, direct3d11.id3d11device3_createquery1
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ID3D11Device3::CreateQuery1
 - d3d11_3/ID3D11Device3::CreateQuery1
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
 - ID3D11Device3.CreateQuery1
---

# ID3D11Device3::CreateQuery1


## -description

Creates a query object for querying information from the graphics processing unit (GPU).

## -parameters

### -param pQueryDesc1 [in]

Type: <b>const <a href="/windows/desktop/api/d3d11_3/ns-d3d11_3-cd3d11_query_desc1">D3D11_QUERY_DESC1</a>*</b>

Pointer to a <a href="/windows/desktop/api/d3d11_3/ns-d3d11_3-cd3d11_query_desc1">D3D11_QUERY_DESC1</a> structure that represents a query description.

### -param ppQuery1 [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11query1">ID3D11Query1</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11query1">ID3D11Query1</a> interface for the created query object. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return <b>S_FALSE</b> if the other input parameters pass validation).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns E_OUTOFMEMORY if there is insufficient memory to create the query object.  
        See <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a> for other possible return values.

## -see-also

<a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11device3">ID3D11Device3</a>