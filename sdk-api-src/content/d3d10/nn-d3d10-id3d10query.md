---
UID: NN:d3d10.ID3D10Query
title: ID3D10Query (d3d10.h)
description: A query interface queries information from the GPU. (ID3D10Query)
helpviewer_keywords: ["44824060-7dfe-0b44-7549-6ab5b12a7e8f","ID3D10Query","ID3D10Query interface [Direct3D 10]","ID3D10Query interface [Direct3D 10]","described","d3d10/ID3D10Query","direct3d10.id3d10query"]
old-location: direct3d10\id3d10query.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10query.htm
ms.date: 12/05/2018
ms.keywords: 44824060-7dfe-0b44-7549-6ab5b12a7e8f, ID3D10Query, ID3D10Query interface [Direct3D 10], ID3D10Query interface [Direct3D 10],described, d3d10/ID3D10Query, direct3d10.id3d10query
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Query
 - d3d10/ID3D10Query
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Query
---

# ID3D10Query interface


## -description

A query interface queries information from the GPU.

## -inheritance

The <b>ID3D10Query</b> interface inherits from <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10asynchronous">ID3D10Asynchronous</a>. <b>ID3D10Query</b> also has these types of members:

## -remarks

A query can be created with <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createquery">ID3D10Device::CreateQuery</a>.

This interface inherits the functionality of an <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10asynchronous">ID3D10Asynchronous Interface</a>.

Query data is typically gathered by issuing an <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-begin">ID3D10Asynchronous::Begin</a> command, issuing some graphics commands, issuing an <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-end">ID3D10Asynchronous::End</a> command, and then calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">ID3D10Asynchronous::GetData</a> to get data about what happened in between the Begin and End calls. The data returned by GetData will be different depending on the type of query.

There are, however, some queries that do not require calls to Begin. For a list of possible queries see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_query">D3D10_QUERY</a>.

A query is typically executed as shown in the following code:


```
D3D10_QUERY_DESC queryDesc;

... // Fill out queryDesc structure

ID3D10Query * pQuery;
pDevice->CreateQuery(&queryDesc, &pQuery);

pQuery->Begin();

... // Issue graphics commands, do whatever

pQuery->End();

UINT64 queryData; // This data type is different depending on the query type

while( S_OK != pQuery->GetData(&queryData, sizeof(UINT64), 0) )
{
}

```


When using a query that does not require a call to Begin, it still requires a call to End. The call to End causes the data returned by GetData to be accurate up until the last call to End.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10asynchronous">ID3D10Asynchronous</a>
