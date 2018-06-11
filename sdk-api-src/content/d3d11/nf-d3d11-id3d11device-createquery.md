---
UID: NF:d3d11.ID3D11Device.CreateQuery
title: ID3D11Device::CreateQuery
author: windows-sdk-content
description: This interface encapsulates methods for querying information from the GPU.
old-location: direct3d11\id3d11device_createquery.htm
old-project: direct3d11
ms.assetid: ad09a309-862f-462d-8268-62e44397c298
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: CreateQuery, CreateQuery method [Direct3D 11], CreateQuery method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateQuery method, ID3D11Device.CreateQuery, ID3D11Device::CreateQuery, d3d11/ID3D11Device::CreateQuery, direct3d11.id3d11device_createquery, f2e88fab-8ad2-a5e2-0d8a-4c97538eb108
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
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
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::CreateQuery


## -description


This interface encapsulates methods for querying information from the GPU.


## -parameters




### -param pQueryDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/2ed8e380-744b-41e1-87c8-9c7e8100ea2f">D3D11_QUERY_DESC</a>*</b>

Pointer to a query description (see <a href="https://msdn.microsoft.com/2ed8e380-744b-41e1-87c8-9c7e8100ea2f">D3D11_QUERY_DESC</a>).


### -param ppQuery [out, optional]

Type: <b><a href="https://msdn.microsoft.com/d296a5aa-147c-460d-acc6-e097ea503378">ID3D11Query</a>**</b>

Address of a pointer to the query object created (see <a href="https://msdn.microsoft.com/d296a5aa-147c-460d-acc6-e097ea503378">ID3D11Query</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns E_OUTOFMEMORY if there is insufficient memory to create the query object.  
        See <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a> for other possible return values.




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

