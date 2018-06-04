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

# ID3D11Counter interface


## -description


This interface encapsulates methods for measuring GPU performance.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Counter</b> interface inherits from <a href="https://msdn.microsoft.com/37ff9dc0-5ec2-4cd5-b252-44e2dac45355">ID3D11Asynchronous</a>. <b>ID3D11Counter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Counter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2422b2d3-29c1-40cf-a41a-f9f299c2d436">GetDesc</a>
</td>
<td align="left" width="63%">
Get a counter description.

</td>
</tr>
</table> 


## -remarks



A counter can be created with <a href="https://msdn.microsoft.com/857111cc-f590-4383-994c-a72402f8a4aa">ID3D11Device::CreateCounter</a>.

This is a derived class of <a href="https://msdn.microsoft.com/37ff9dc0-5ec2-4cd5-b252-44e2dac45355">ID3D11Asynchronous</a>.

Counter data is gathered by issuing an <a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">ID3D11DeviceContext::Begin</a> command, issuing some graphics commands, issuing an <a href="https://msdn.microsoft.com/9b941abc-04a3-4dd7-b72d-62cd5bd06b47">ID3D11DeviceContext::End</a> command, and then calling <a href="https://msdn.microsoft.com/338d02ad-2227-49e5-9b4f-fb86a3898f73">ID3D11DeviceContext::GetData</a> to get data about what happened in between the Begin and End calls. The data returned by GetData will be different depending on the type of counter. The call to End causes the data returned by GetData to be accurate up until the last call to End.

Counters are best suited for profiling.

For a list of the types of performance counters, see <a href="https://msdn.microsoft.com/b6a5cc7e-48e5-478a-aa9c-8b2878c0de6b">D3D11_COUNTER</a>.




## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/37ff9dc0-5ec2-4cd5-b252-44e2dac45355">ID3D11Asynchronous</a>
 

 

