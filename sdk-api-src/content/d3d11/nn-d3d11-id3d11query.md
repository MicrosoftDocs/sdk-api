---
UID: NN:d3d11.ID3D11Query
title: ID3D11Query
author: windows-sdk-content
description: A query interface queries information from the GPU.
old-location: direct3d11\id3d11query.htm
old-project: direct3d11
ms.assetid: d296a5aa-147c-460d-acc6-e097ea503378
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 0779360e-d58a-0694-026e-d85fdc97bf60, ID3D11Query, ID3D11Query interface [Direct3D 11], ID3D11Query interface [Direct3D 11],described, d3d11/ID3D11Query, direct3d11.id3d11query
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
 - ID3D11Query
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Query interface


## -description


A query interface queries information from the GPU.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Query</b> interface inherits from <a href="https://msdn.microsoft.com/37ff9dc0-5ec2-4cd5-b252-44e2dac45355">ID3D11Asynchronous</a>. <b>ID3D11Query</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7eca470a-98ff-450a-8ff9-3b929ff70deb">GetDesc</a>
</td>
<td align="left" width="63%">
Get a query description.

</td>
</tr>
</table> 


## -remarks



A query can be created with <a href="https://msdn.microsoft.com/ad09a309-862f-462d-8268-62e44397c298">ID3D11Device::CreateQuery</a>.

Query data is typically gathered by issuing an <a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">ID3D11DeviceContext::Begin</a> command, issuing some graphics commands, issuing an <a href="https://msdn.microsoft.com/9b941abc-04a3-4dd7-b72d-62cd5bd06b47">ID3D11DeviceContext::End</a> command, and then calling <a href="https://msdn.microsoft.com/338d02ad-2227-49e5-9b4f-fb86a3898f73">ID3D11DeviceContext::GetData</a> to get data about what happened in between the Begin and End calls. The data returned by <b>GetData</b> will be different depending on the type of query.

There are, however, some queries that do not require calls to <a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">Begin</a>. For a list of possible queries see <a href="https://msdn.microsoft.com/4161fbeb-7f58-422c-a195-ea10f737fd0c">D3D11_QUERY</a>.

A query is typically executed as shown in the following code:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>

D3D11_QUERY_DESC queryDesc;
... // Fill out queryDesc structure
ID3D11Query * pQuery;
pDevice-&gt;CreateQuery(&amp;queryDesc, &amp;pQuery);
pDeviceContext-&gt;Begin(pQuery);

... // Issue graphics commands

pDeviceContext-&gt;End(pQuery);
UINT64 queryData; // This data type is different depending on the query type

while( S_OK != pDeviceContext-&gt;GetData(pQuery, &amp;queryData, sizeof(UINT64), 0) )
{
}
</pre>
</td>
</tr>
</table></span></div>
When using a query that does not require a call to <a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">Begin</a>, it still requires a call to <a href="https://msdn.microsoft.com/9b941abc-04a3-4dd7-b72d-62cd5bd06b47">End</a>. The call to <b>End</b> causes the data returned by <a href="https://msdn.microsoft.com/library/windows/hardware/dn949631">GetData</a> to be accurate up until the last call to <b>End</b>.




## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/37ff9dc0-5ec2-4cd5-b252-44e2dac45355">ID3D11Asynchronous</a>
 

 

