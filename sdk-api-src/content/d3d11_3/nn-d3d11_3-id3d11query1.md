---
UID: NN:d3d11_3.ID3D11Query1
title: ID3D11Query1
author: windows-sdk-content
description: Represents a query object for querying information from the graphics processing unit (GPU).
old-location: direct3d11\id3d11query1.htm
old-project: direct3d11
ms.assetid: 6DF4364F-A20D-466E-8F26-17C6DD32E84B
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: ID3D11Query1, ID3D11Query1 interface [Direct3D 11], ID3D11Query1 interface [Direct3D 11],described, d3d11_3/ID3D11Query1, direct3d11.id3d11query1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_TEXTURE_LAYOUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11Query1
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
---

# ID3D11Query1 interface


## -description


Represents a query object for querying information from the graphics processing unit (GPU).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Query1</b> interface inherits from <a href="https://msdn.microsoft.com/d296a5aa-147c-460d-acc6-e097ea503378">ID3D11Query</a>. <b>ID3D11Query1</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/79F8F200-CF4E-4587-A31E-8A67C4418898">GetDesc1</a>
</td>
<td align="left" width="63%">
Gets a query description.

</td>
</tr>
</table> 


## -remarks



A query can be created with <a href="https://msdn.microsoft.com/8D170F97-DA95-48FE-84F6-2BBB3E388BB4">ID3D11Device3::CreateQuery1</a>.

Query data is typically gathered by issuing an <a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">ID3D11DeviceContext::Begin</a> command, issuing some graphics commands, issuing an <a href="https://msdn.microsoft.com/9b941abc-04a3-4dd7-b72d-62cd5bd06b47">ID3D11DeviceContext::End</a> command, and then calling <a href="https://msdn.microsoft.com/338d02ad-2227-49e5-9b4f-fb86a3898f73">ID3D11DeviceContext::GetData</a> to get data about what happened in between the Begin and End calls. The data returned by <b>GetData</b> will be different depending on the type of query.

There are, however, some queries that do not require calls to <a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">Begin</a>. For a list of possible queries see <a href="https://msdn.microsoft.com/4161fbeb-7f58-422c-a195-ea10f737fd0c">D3D11_QUERY</a>.

When using a query that does not require a call to <a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">Begin</a>, it still requires a call to <a href="https://msdn.microsoft.com/9b941abc-04a3-4dd7-b72d-62cd5bd06b47">End</a>. The call to <b>End</b> causes the data returned by <a href="https://msdn.microsoft.com/library/windows/hardware/dn949631">GetData</a> to be accurate up until the last call to <b>End</b>.




## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/d296a5aa-147c-460d-acc6-e097ea503378">ID3D11Query</a>
 

 

