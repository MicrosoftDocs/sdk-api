---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDirect3DDevice9::CreateQuery


## -description


Creates a status query.


## -parameters




### -param Type [in]

Type: <b><a href="https://msdn.microsoft.com/575c4e71-3cab-4123-a2a5-d23b53e87111">D3DQUERYTYPE</a></b>

Identifies the query type. For more information, see <a href="https://msdn.microsoft.com/575c4e71-3cab-4123-a2a5-d23b53e87111">D3DQUERYTYPE</a>.


### -param ppQuery [out, retval]

Type: <b><a href="https://msdn.microsoft.com/7f25d64e-ece6-4544-ada0-5cc3d34b88e6">IDirect3DQuery9</a>**</b>

Returns a pointer to the query interface that manages the query object. See <a href="https://msdn.microsoft.com/7f25d64e-ece6-4544-ada0-5cc3d34b88e6">IDirect3DQuery9</a>. 

This parameter can be set to <b>NULL</b> to see if a query is supported. If the query is not supported, the method returns D3DERR_NOTAVAILABLE.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_NOTAVAILABLE or  E_OUTOFMEMORY.




## -remarks



This method is provided for both synchronous and asynchronous queries. It takes the place of GetInfo, which is no longer supported in Direct3D 9.

Synchronous and asynchronous queries are created with <b>IDirect3DDevice9::CreateQuery</b> with <a href="https://msdn.microsoft.com/575c4e71-3cab-4123-a2a5-d23b53e87111">D3DQUERYTYPE</a>. When a query has been created and the API calls have been made that are being queried, use <a href="https://msdn.microsoft.com/8b9a9b1d-bc00-4961-b8ed-edbbf4e64fda">IDirect3DQuery9::Issue</a> to issue a query and  <a href="https://msdn.microsoft.com/5363b5a4-6ac1-4f4e-8d64-949968d2a08a">IDirect3DQuery9::GetData</a> to get the results of the query.




## -see-also




<a href="https://msdn.microsoft.com/81e1c5c5-03bc-4598-814e-14e56513e221">Asynchronous Notification (Direct3D 9)</a>



<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

