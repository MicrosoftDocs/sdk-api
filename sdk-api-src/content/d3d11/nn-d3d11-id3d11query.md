---
UID: NN:d3d11.ID3D11Query
title: ID3D11Query (d3d11.h)
author: windows-sdk-content
description: A query interface queries information from the GPU.
old-location: direct3d11\id3d11query.htm
tech.root: direct3d11
ms.assetid: d296a5aa-147c-460d-acc6-e097ea503378
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 0779360e-d58a-0694-026e-d85fdc97bf60, ID3D11Query, ID3D11Query interface [Direct3D 11], ID3D11Query interface [Direct3D 11],described, d3d11/ID3D11Query, direct3d11.id3d11query
ms.topic: interface
f1_keywords: 
 - "d3d11/ID3D11Query"
dev_langs:
 - c++
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Query
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11Query interface


## -description


A query interface queries information from the GPU.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Query</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11asynchronous">ID3D11Asynchronous</a>. <b>ID3D11Query</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Query</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11query-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get a query description.

</td>
</tr>
</table> 


## -remarks



A query can be created with <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createquery">ID3D11Device::CreateQuery</a>.

Query data is typically gathered by issuing an <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> command, issuing some graphics commands, issuing an <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a> command, and then calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> to get data about what happened in between the Begin and End calls. The data returned by <b>GetData</b> will be different depending on the type of query.

There are, however, some queries that do not require calls to <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">Begin</a>. For a list of possible queries see <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ne-d3d11-d3d11_query">D3D11_QUERY</a>.

A query is typically executed as shown in the following code:


```


D3D11_QUERY_DESC queryDesc;
... // Fill out queryDesc structure
ID3D11Query * pQuery;
pDevice->CreateQuery(&queryDesc, &pQuery);
pDeviceContext->Begin(pQuery);

... // Issue graphics commands

pDeviceContext->End(pQuery);
UINT64 queryData; // This data type is different depending on the query type

while( S_OK != pDeviceContext->GetData(pQuery, &queryData, sizeof(UINT64), 0) )
{
}

```


When using a query that does not require a call to <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">Begin</a>, it still requires a call to <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">End</a>. The call to <b>End</b> causes the data returned by <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">GetData</a> to be accurate up until the last call to <b>End</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11asynchronous">ID3D11Asynchronous</a>
 

 

