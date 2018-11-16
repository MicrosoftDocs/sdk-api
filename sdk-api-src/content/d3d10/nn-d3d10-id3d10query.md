---
UID: NN:d3d10.ID3D10Query
title: ID3D10Query
author: windows-sdk-content
description: A query interface queries information from the GPU.
old-location: direct3d10\id3d10query.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10query.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 44824060-7dfe-0b44-7549-6ab5b12a7e8f, ID3D10Query, ID3D10Query interface [Direct3D 10], ID3D10Query interface [Direct3D 10],described, d3d10/ID3D10Query, direct3d10.id3d10query
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Query interface


## -description


A query interface queries information from the GPU.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Query</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb173500(v=VS.85).aspx">ID3D10Asynchronous</a>. <b>ID3D10Query</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D10Query</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173824(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get a query description.

</td>
</tr>
</table> 


## -remarks



A query can be created with <a href="https://msdn.microsoft.com/en-us/library/Bb173553(v=VS.85).aspx">ID3D10Device::CreateQuery</a>.

This interface inherits the functionality of an <a href="https://msdn.microsoft.com/en-us/library/Bb173500(v=VS.85).aspx">ID3D10Asynchronous Interface</a>.

Query data is typically gathered by issuing an <a href="https://msdn.microsoft.com/en-us/library/Bb173501(v=VS.85).aspx">ID3D10Asynchronous::Begin</a> command, issuing some graphics commands, issuing an <a href="https://msdn.microsoft.com/en-us/library/Bb173502(v=VS.85).aspx">ID3D10Asynchronous::End</a> command, and then calling <a href="https://msdn.microsoft.com/en-us/library/Bb173503(v=VS.85).aspx">ID3D10Asynchronous::GetData</a> to get data about what happened in between the Begin and End calls. The data returned by GetData will be different depending on the type of query.

There are, however, some queries that do not require calls to Begin. For a list of possible queries see <a href="https://msdn.microsoft.com/en-us/library/Bb205335(v=VS.85).aspx">D3D10_QUERY</a>.

A query is typically executed as shown in the following code:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>D3D10_QUERY_DESC queryDesc;

... // Fill out queryDesc structure

ID3D10Query * pQuery;
pDevice-&gt;CreateQuery(&amp;queryDesc, &amp;pQuery);

pQuery-&gt;Begin();

... // Issue graphis commands, do whatever

pQuery-&gt;End();

UINT64 queryData; // This data type is different depending on the query type

while( S_OK != pQuery-&gt;GetData(&amp;queryData, sizeof(UINT64), 0) )
{
}
</pre>
</td>
</tr>
</table></span></div>
When using a query that does not require a call to Begin, it still requires a call to End. The call to End causes the data returned by GetData to be accurate up until the last call to End.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205152(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173500(v=VS.85).aspx">ID3D10Asynchronous</a>
 

 

