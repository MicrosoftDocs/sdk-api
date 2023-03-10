---
UID: NF:d3d9.IDirect3DDevice9.CreateQuery
title: IDirect3DDevice9::CreateQuery (d3d9.h)
description: The IDirect3DDevice9::CreateQuery method (d3d9.h) creates a status query.
helpviewer_keywords: ["10c37273-2f16-3b39-a1ff-6d476ef75dd7","CreateQuery","CreateQuery method [Direct3D 9]","CreateQuery method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","CreateQuery method","IDirect3DDevice9.CreateQuery","IDirect3DDevice9::CreateQuery","d3d9helper/IDirect3DDevice9::CreateQuery","direct3d9.idirect3ddevice9__createquery"]
old-location: direct3d9\idirect3ddevice9__createquery.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createquery.htm
ms.date: 08/10/2022
ms.keywords: 10c37273-2f16-3b39-a1ff-6d476ef75dd7, CreateQuery, CreateQuery method [Direct3D 9], CreateQuery method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateQuery method, IDirect3DDevice9.CreateQuery, IDirect3DDevice9::CreateQuery, d3d9helper/IDirect3DDevice9::CreateQuery, direct3d9.idirect3ddevice9__createquery
req.header: d3d9.h
req.include-header: D3D9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9::CreateQuery
 - d3d9/IDirect3DDevice9::CreateQuery
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.CreateQuery
---

# IDirect3DDevice9::CreateQuery


## -description

Creates a status query.

## -parameters

### -param Type [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dquerytype">D3DQUERYTYPE</a></b>

Identifies the query type. For more information, see <a href="/windows/desktop/direct3d9/d3dquerytype">D3DQUERYTYPE</a>.

### -param ppQuery [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9">IDirect3DQuery9</a>**</b>

Returns a pointer to the query interface that manages the query object. See <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9">IDirect3DQuery9</a>. 

This parameter can be set to <b>NULL</b> to see if a query is supported. If the query is not supported, the method returns D3DERR_NOTAVAILABLE.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_NOTAVAILABLE or  E_OUTOFMEMORY.

## -remarks

This method is provided for both synchronous and asynchronous queries. It takes the place of GetInfo, which is no longer supported in Direct3D 9.

Synchronous and asynchronous queries are created with <b>IDirect3DDevice9::CreateQuery</b> with <a href="/windows/desktop/direct3d9/d3dquerytype">D3DQUERYTYPE</a>. When a query has been created and the API calls have been made that are being queried, use <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue">IDirect3DQuery9::Issue</a> to issue a query and  <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata">IDirect3DQuery9::GetData</a> to get the results of the query.

## -see-also

<a href="/windows/desktop/direct3d9/asynchronous-notification">Asynchronous Notification (Direct3D 9)</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
