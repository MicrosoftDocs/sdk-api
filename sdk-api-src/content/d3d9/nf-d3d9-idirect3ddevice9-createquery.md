---
UID: NF:d3d9.IDirect3DDevice9.CreateQuery
title: IDirect3DDevice9::CreateQuery
author: windows-sdk-content
description: Creates a status query.
old-location: direct3d9\idirect3ddevice9__createquery.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createquery.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 10c37273-2f16-3b39-a1ff-6d476ef75dd7, CreateQuery, CreateQuery method [Direct3D 9], CreateQuery method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateQuery method, IDirect3DDevice9.CreateQuery, IDirect3DDevice9::CreateQuery, d3d9helper/IDirect3DDevice9::CreateQuery, direct3d9.idirect3ddevice9__createquery
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
req.include-header: D3D9.h
req.redist: 
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
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
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
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::CreateQuery


## -description


Creates a status query.


## -parameters




### -param Type [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172594(v=VS.85).aspx">D3DQUERYTYPE</a></b>

Identifies the query type. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb172594(v=VS.85).aspx">D3DQUERYTYPE</a>.


### -param ppQuery [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205872(v=VS.85).aspx">IDirect3DQuery9</a>**</b>

Returns a pointer to the query interface that manages the query object. See <a href="https://msdn.microsoft.com/en-us/library/Bb205872(v=VS.85).aspx">IDirect3DQuery9</a>. 

This parameter can be set to <b>NULL</b> to see if a query is supported. If the query is not supported, the method returns D3DERR_NOTAVAILABLE.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_NOTAVAILABLE or  E_OUTOFMEMORY.




## -remarks



This method is provided for both synchronous and asynchronous queries. It takes the place of GetInfo, which is no longer supported in Direct3D 9.

Synchronous and asynchronous queries are created with <b>IDirect3DDevice9::CreateQuery</b> with <a href="https://msdn.microsoft.com/en-us/library/Bb172594(v=VS.85).aspx">D3DQUERYTYPE</a>. When a query has been created and the API calls have been made that are being queried, use <a href="https://msdn.microsoft.com/en-us/library/Bb205877(v=VS.85).aspx">IDirect3DQuery9::Issue</a> to issue a query and  <a href="https://msdn.microsoft.com/en-us/library/Bb205873(v=VS.85).aspx">IDirect3DQuery9::GetData</a> to get the results of the query.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb172276(v=VS.85).aspx">Asynchronous Notification (Direct3D 9)</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>
 

 

