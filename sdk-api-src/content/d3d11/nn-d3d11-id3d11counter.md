---
UID: NN:d3d11.ID3D11Counter
title: ID3D11Counter
author: windows-sdk-content
description: This interface encapsulates methods for measuring GPU performance.
old-location: direct3d11\id3d11counter.htm
tech.root: direct3d11
ms.assetid: 3f35b3d5-f829-443c-9ea6-6cffdd4f58b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11Counter, ID3D11Counter interface [Direct3D 11], ID3D11Counter interface [Direct3D 11],described, d3d11/ID3D11Counter, direct3d11.id3d11counter, e8e19b70-2584-4e44-1faf-1bc2d275606a
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ID3D11Counter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Counter interface


## -description


This interface encapsulates methods for measuring GPU performance.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Counter</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476347(v=VS.85).aspx">ID3D11Asynchronous</a>. <b>ID3D11Counter</b> also has these types of members:
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

This is a derived class of <a href="https://msdn.microsoft.com/en-us/library/Ff476347(v=VS.85).aspx">ID3D11Asynchronous</a>.

Counter data is gathered by issuing an <a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">ID3D11DeviceContext::Begin</a> command, issuing some graphics commands, issuing an <a href="https://msdn.microsoft.com/9b941abc-04a3-4dd7-b72d-62cd5bd06b47">ID3D11DeviceContext::End</a> command, and then calling <a href="https://msdn.microsoft.com/en-us/library/Ff476428(v=VS.85).aspx">ID3D11DeviceContext::GetData</a> to get data about what happened in between the Begin and End calls. The data returned by GetData will be different depending on the type of counter. The call to End causes the data returned by GetData to be accurate up until the last call to End.

Counters are best suited for profiling.

For a list of the types of performance counters, see <a href="https://msdn.microsoft.com/en-us/library/Ff476102(v=VS.85).aspx">D3D11_COUNTER</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476154(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476347(v=VS.85).aspx">ID3D11Asynchronous</a>
 

 

