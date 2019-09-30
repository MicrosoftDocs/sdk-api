---
UID: NN:d3d11_3.ID3D11Query1
title: ID3D11Query1 (d3d11_3.h)
author: windows-sdk-content
description: Represents a query object for querying information from the graphics processing unit (GPU).
old-location: direct3d11\id3d11query1.htm
tech.root: direct3d11
ms.assetid: 6DF4364F-A20D-466E-8F26-17C6DD32E84B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11Query1, ID3D11Query1 interface [Direct3D 11], ID3D11Query1 interface [Direct3D 11],described, d3d11_3/ID3D11Query1, direct3d11.id3d11query1
ms.topic: interface
f1_keywords: 
 - "d3d11_3/ID3D11Query1"
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - ID3D11Query1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11Query1 interface


## -description


Represents a query object for querying information from the graphics processing unit (GPU).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Query1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11query">ID3D11Query</a>. <b>ID3D11Query1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Query1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11query1-getdesc1">GetDesc1</a>
</td>
<td align="left" width="63%">
Gets a query description.

</td>
</tr>
</table> 


## -remarks



A query can be created with <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createquery1">ID3D11Device3::CreateQuery1</a>.

Query data is typically gathered by issuing an <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> command, issuing some graphics commands, issuing an <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a> command, and then calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> to get data about what happened in between the Begin and End calls. The data returned by <b>GetData</b> will be different depending on the type of query.

There are, however, some queries that do not require calls to <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">Begin</a>. For a list of possible queries see <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ne-d3d11-d3d11_query">D3D11_QUERY</a>.

When using a query that does not require a call to <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">Begin</a>, it still requires a call to <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">End</a>. The call to <b>End</b> causes the data returned by <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">GetData</a> to be accurate up until the last call to <b>End</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11query">ID3D11Query</a>
 

 

