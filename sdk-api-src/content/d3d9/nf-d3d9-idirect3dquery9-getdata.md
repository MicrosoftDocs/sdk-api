---
UID: NF:d3d9.IDirect3DQuery9.GetData
title: IDirect3DQuery9::GetData (d3d9.h)
description: The IDirect3DQuery9::GetData method (d3d9.h) polls a queried resource to get the query state or a query result. 
helpviewer_keywords: ["61a50651-865a-2305-3acc-ca22ba941030","GetData","GetData method [Direct3D 9]","GetData method [Direct3D 9]","IDirect3DQuery9 interface","IDirect3DQuery9 interface [Direct3D 9]","GetData method","IDirect3DQuery9.GetData","IDirect3DQuery9::GetData","d3d9helper/IDirect3DQuery9::GetData","direct3d9.idirect3dquery9__getdata"]
old-location: direct3d9\idirect3dquery9__getdata.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dquery9__getdata.htm
ms.date: 08/11/2022
ms.keywords: 61a50651-865a-2305-3acc-ca22ba941030, GetData, GetData method [Direct3D 9], GetData method [Direct3D 9],IDirect3DQuery9 interface, IDirect3DQuery9 interface [Direct3D 9],GetData method, IDirect3DQuery9.GetData, IDirect3DQuery9::GetData, d3d9helper/IDirect3DQuery9::GetData, direct3d9.idirect3dquery9__getdata
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
 - IDirect3DQuery9::GetData
 - d3d9/IDirect3DQuery9::GetData
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
 - IDirect3DQuery9.GetData
---

# IDirect3DQuery9::GetData


## -description

Polls a queried resource to get the query state or a query result. For more information about queries, see <a href="/windows/desktop/direct3d9/queries">Queries (Direct3D 9)</a>.

## -parameters

### -param pData [in, out]

Type: <b>void*</b>

Pointer to a buffer containing the query data. The user is responsible for allocating this. <i>pData</i> may be <b>NULL</b> only if dwSize is 0.

### -param dwSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Number of bytes of data in <i>pData</i>. If you set dwSize to zero, you can use this method to poll the resource for the query status. See remarks.

### -param dwGetDataFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Data flags specifying the query type. Valid values are either 0 or <a href="/windows/desktop/direct3d9/d3dgetdata-flush">D3DGETDATA_FLUSH</a>. Use 0 to avoid flushing batched queries to the driver and use D3DGETDATA_FLUSH to go ahead and flush them. For applications writing their own version of waiting, a query result is not realized until the driver receives a flush.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

The return type identifies the query state (see <a href="/windows/desktop/direct3d9/queries">Queries (Direct3D 9)</a>). The method returns S_OK if the query data is available and S_FALSE if it is not.  These are considered successful return values. If the method fails when <a href="/windows/desktop/direct3d9/d3dgetdata-flush">D3DGETDATA_FLUSH</a> is used, the return value can be D3DERR_DEVICELOST.

## -remarks

It is possible to lose the device while polling for query status. When <a href="/windows/desktop/direct3d9/d3dgetdata-flush">D3DGETDATA_FLUSH</a> is specified, this method will return D3DERR_DEVICELOST in response to a lost device. This allows an application to prevent threads from endlessly polling due to a lost device (which cannot respond to the query).

An application must never write code that only invokes GetData ( ... , 0 ), expecting that GetData will eventually return S_OK by itself over time. This is true, even if the application has used the FLUSH flag with GetData in the past. For example:


```
// Enables an infinite loop:
while( pQuery->GetData( ... , 0 ) == S_FALSE ) ;

// Still enables an infinite loop:
pQuery->GetData( ... , D3DGETDATA_FLUSH );
while( pQuery->GetData( ... , 0 ) == S_FALSE ) ;

// Does not enable an infinite loop because eventually the command
// buffer will fill up and that will cause a flush to occur.
while( pQuery->GetData( ..., 0 ) == S_FALSE ) {
	pDevice->SetTexture(...);
	pDevice->Draw(...);
}

```

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9">IDirect3DQuery9</a>
