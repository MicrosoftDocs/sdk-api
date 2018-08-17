---
UID: NN:d3d10.ID3D10Counter
title: ID3D10Counter
author: windows-sdk-content
description: This interface encapsulates methods for measuring GPU performance.
old-location: direct3d10\id3d10counter.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10counter.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 004d04e1-a54d-6c89-c551-db2d30d9d7e9, ID3D10Counter, ID3D10Counter interface [Direct3D 10], ID3D10Counter interface [Direct3D 10],described, d3d10/ID3D10Counter, direct3d10.id3d10counter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10.h
req.include-header: 
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Counter
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Counter interface


## -description


This interface encapsulates methods for measuring GPU performance.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Counter</b> interface inherits from <a href="https://msdn.microsoft.com/71ed9ae8-d1a1-442c-ac0f-6b4ede613bfb">ID3D10Asynchronous</a>. <b>ID3D10Counter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10Counter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58e542fb-ba29-4b57-a752-e3a467cc501e">GetDesc</a>
</td>
<td align="left" width="63%">
Get a counter description.

</td>
</tr>
</table> 


## -remarks



A counter can be created with <a href="https://msdn.microsoft.com/bead7e2d-3d29-4b41-87f7-b821a4ffb78a">ID3D10Device::CreateCounter</a>.

This is a derived class of <a href="https://msdn.microsoft.com/71ed9ae8-d1a1-442c-ac0f-6b4ede613bfb">ID3D10Asynchronous Interface</a>.

Counter data is gathered by issuing an <a href="https://msdn.microsoft.com/53ae44d0-822b-4fc9-ac77-814ac73eb08a">ID3D10Asynchronous::Begin</a> command, issuing some graphics commands, issuing an <a href="https://msdn.microsoft.com/147a93b4-7151-4800-8aa5-286058f49ee8">ID3D10Asynchronous::End</a> command, and then calling <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">ID3D10Asynchronous::GetData</a> to get data about what happened in between the Begin and End calls. The data returned by GetData will be different depending on the type of counter. The call to End causes the data returned by GetData to be accurate up until the last call to End.

Counters are best suited for profiling.

For a list of the types of performance counters, see <a href="https://msdn.microsoft.com/b4c63ba3-29cf-4fb9-903f-28ac7750f9b6">D3D10_COUNTER</a>.




## -see-also




<a href="https://msdn.microsoft.com/f5ad2db8-da90-4bcd-83a7-7466723a9c3c">Core Interfaces</a>



<a href="https://msdn.microsoft.com/71ed9ae8-d1a1-442c-ac0f-6b4ede613bfb">ID3D10Asynchronous</a>
 

 

