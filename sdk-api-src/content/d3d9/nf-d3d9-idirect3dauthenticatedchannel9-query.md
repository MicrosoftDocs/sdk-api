---
UID: NF:d3d9.IDirect3DAuthenticatedChannel9.Query
title: IDirect3DAuthenticatedChannel9::Query
author: windows-sdk-content
description: Sends a query to the authenticated channel.
old-location: mf\idirect3dauthenticatedchannel9_query.htm
old-project: medfound
ms.assetid: 370ed31d-5b75-4767-b8d8-33cb2ff49fee
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IDirect3DAuthenticatedChannel9 interface [Media Foundation],Query method, IDirect3DAuthenticatedChannel9.Query, IDirect3DAuthenticatedChannel9::Query, Query, Query method [Media Foundation], Query method [Media Foundation],IDirect3DAuthenticatedChannel9 interface, d3d9/IDirect3DAuthenticatedChannel9::Query, mf.idirect3dauthenticatedchannel9_query
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - d3d9.h
api_name:
 - IDirect3DAuthenticatedChannel9.Query
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirect3DAuthenticatedChannel9::Query


## -description


Sends a query to the authenticated channel.


## -parameters




### -param InputSize

The size of the <i>pInput</i> array, in bytes.


### -param pInput

A pointer to a byte array that contains input data for the query. This array always starts with a <a href="https://msdn.microsoft.com/6a484652-8da2-4074-96b2-6fe49f4d4200">D3DAUTHENTICATEDCHANNEL_QUERY_INPUT</a> structure. The <b>QueryType</b> member of the structure specifies the query and defines the meaning of the rest of the array.


### -param OutputSize

The size of the <i>pOutput</i> array, in bytes.


### -param pOutput

A pointer to a byte array that receives the result of the query. This array always starts with a <a href="https://msdn.microsoft.com/b2783b8e-0436-419a-a93e-93dc1b87024d">D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT</a> structure. The meaning of the rest of the array depends on the query.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For a list of queries, see <a href="https://msdn.microsoft.com/75e246c6-bf23-44d9-8fb3-46a6dc5324a5">Content Protection Queries</a>. 




## -see-also




<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>



<a href="https://msdn.microsoft.com/dd969956-a140-44ed-9917-5a0a09a432fa">IDirect3DAuthenticatedChannel9</a>
 

 

