---
UID: NN:d3d11_4.ID3D11Multithread
title: ID3D11Multithread
author: windows-sdk-content
description: Provides threading protection for critical sections of a multi-threaded application.
old-location: direct3d11\id3d11multithread.htm
old-project: direct3d11
ms.assetid: 1A07694E-7D61-4A59-82E3-048F04C8D57A
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: ID3D11Multithread, ID3D11Multithread interface [Direct3D 11], ID3D11Multithread interface [Direct3D 11],described, d3d11_4/ID3D11Multithread, direct3d11.id3d11multithread
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11_4.h
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
req.typenames: D3D11_UNORDERED_ACCESS_VIEW_DESC1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_4.dll
api_name:
 - ID3D11Multithread
product: Windows
targetos: Windows
req.lib: D3d11_4.lib
req.dll: D3d11_4.dll
req.irql: 
---

# ID3D11Multithread interface


## -description


Provides threading protection for critical sections of a multi-threaded application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Multithread</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11Multithread</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Multithread</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A742D03A-0A47-4B08-952A-836A272D1519">Enter</a>
</td>
<td align="left" width="63%">
Enter a device's critical section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1BCB0021-9C92-425D-97C1-6EDB1D2127A8">GetMultithreadProtected</a>
</td>
<td align="left" width="63%">
Find out if multithread protection is turned on or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CECBE440-3F9E-4649-B257-BAD3E7F5CF2F">Leave</a>
</td>
<td align="left" width="63%">
Leave a device's critical section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E8BF9A25-CCEA-44F3-AE7C-376E5B672079">SetMultithreadProtected</a>
</td>
<td align="left" width="63%">
Turns multithread protection on or off.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by querying it from an immediate device context created with the <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> (or later versions of this) interface 
          using <a href="http://msdn.microsoft.com/en-us/library/ms682521(VS.85).aspx">IUnknown::QueryInterface</a>.

Unlike D3D10, there is no multithreaded layer in D3D11. By default, multithread protection is turned off. Use <a href="https://msdn.microsoft.com/E8BF9A25-CCEA-44F3-AE7C-376E5B672079">SetMultithreadProtected</a> to turn it on, then <a href="https://msdn.microsoft.com/A742D03A-0A47-4B08-952A-836A272D1519">Enter</a> and <a href="https://msdn.microsoft.com/CECBE440-3F9E-4649-B257-BAD3E7F5CF2F">Leave</a> to encapsulate graphics commands that  must be executed in a specific order.

By default in D3D11, applications can only use one thread with the immediate context at a time. But, applications can use this interface to change that restriction. The interface can turn on threading protection for the immediate context, which will increase the overhead of each immediate context call in order to share one context with multiple threads.




## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

