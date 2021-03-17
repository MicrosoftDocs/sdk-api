---
UID: NF:d3d11.ID3D11DeviceContext.GetData
title: ID3D11DeviceContext::GetData (d3d11.h)
description: Get data from the graphics processing unit (GPU) asynchronously.
helpviewer_keywords: ["234bd2fb-b886-b634-e4ec-4301f8dd951d","GetData","GetData method [Direct3D 11]","GetData method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","GetData method","ID3D11DeviceContext.GetData","ID3D11DeviceContext::GetData","d3d11/ID3D11DeviceContext::GetData","direct3d11.id3d11devicecontext_getdata"]
old-location: direct3d11\id3d11devicecontext_getdata.htm
tech.root: direct3d11
ms.assetid: 338d02ad-2227-49e5-9b4f-fb86a3898f73
ms.date: 12/05/2018
ms.keywords: 234bd2fb-b886-b634-e4ec-4301f8dd951d, GetData, GetData method [Direct3D 11], GetData method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],GetData method, ID3D11DeviceContext.GetData, ID3D11DeviceContext::GetData, d3d11/ID3D11DeviceContext::GetData, direct3d11.id3d11devicecontext_getdata
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
 - ID3D11DeviceContext::GetData
 - d3d11/ID3D11DeviceContext::GetData
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
 - ID3D11DeviceContext.GetData
---

# ID3D11DeviceContext::GetData


## -description

Get data from the graphics processing unit (GPU) asynchronously.

## -parameters

### -param pAsync [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11asynchronous">ID3D11Asynchronous</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11asynchronous">ID3D11Asynchronous</a> interface for the object about which <b>GetData</b> retrieves data.

### -param pData [out, optional]

Type: <b>void*</b>

Address of memory that will receive the data. If <b>NULL</b>, <b>GetData</b> will be used only to check status. The type of data output depends on the type of asynchronous interface.

### -param DataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the data to retrieve or 0. Must be 0 when <i>pData</i> is <b>NULL</b>.

### -param GetDataFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Optional flags. Can be 0 or any combination of the flags enumerated by <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_async_getdata_flag">D3D11_ASYNC_GETDATA_FLAG</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>. A return value of S_OK indicates that the data at <i>pData</i> is available for the calling application to access. A return value of S_FALSE indicates that the data is not yet available. If the data is not yet available, the application must call <b>GetData</b> until the data is available.

## -remarks

Queries in a deferred context are limited to predicated drawing. That is, you cannot call <b>ID3D11DeviceContext::GetData</b> on a deferred context to get data about a query; you can only call <b>GetData</b> on the immediate context to get data about a query. For predicated drawing, the results of a predication-type query are used by the GPU and not returned to an application. For more information about predication and predicated drawing, see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-setpredication">D3D11DeviceContext::SetPredication</a>.

<b>GetData</b> retrieves the data that the runtime collected between calls to <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>.  Certain queries only require a call to <b>ID3D11DeviceContext::End</b> in which case the data returned by <b>GetData</b> is accurate up to the last call to <b>ID3D11DeviceContext::End</b>. For information about the queries that only require a call to <b>ID3D11DeviceContext::End</b> and about the type of data that <b>GetData</b> retrieves for each query, see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_query">D3D11_QUERY</a>.

If <i>DataSize</i> is 0, <b>GetData</b> is only used to check status.

An application gathers counter data by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a>, issuing some graphics commands, calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>, and then calling <b>ID3D11DeviceContext::GetData</b> to get data about what happened in between the <b>Begin</b> and <b>End</b> calls. For information about performance counter types, see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_counter">D3D11_COUNTER</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>