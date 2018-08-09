---
UID: NN:d3d10.ID3D10Multithread
title: ID3D10Multithread
author: windows-sdk-content
description: A multithread interface accesses multithread settings and can only be used if the thread-safe layer is turned on.
old-location: direct3d10\id3d10multithread.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10multithread.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 03af3cb4-f8ff-e677-80ea-33ee09667866, ID3D10Multithread, ID3D10Multithread interface [Direct3D 10], ID3D10Multithread interface [Direct3D 10],described, d3d10/ID3D10Multithread, direct3d10.id3d10multithread
ms.prod: windows
ms.technology: windows-sdk
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
 - ID3D10Multithread
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Multithread interface


## -description


A multithread interface accesses multithread settings and can only be used if the <a href="https://msdn.microsoft.com/19c81383-6ac7-49ea-98a3-bf761a32ab40">thread-safe layer</a> is turned on. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Multithread</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D10Multithread</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10Multithread</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16617f82-f19c-4ec6-93ae-9f0ec4501a49">Enter</a>
</td>
<td align="left" width="63%">
Enter a device's critical section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b3e0e0d-c78c-4bfc-b174-07ed77e880be">GetMultithreadProtected</a>
</td>
<td align="left" width="63%">
Find out if multithreading is turned on or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/739a4659-55db-409c-b67f-9114c205df03">Leave</a>
</td>
<td align="left" width="63%">
Leave a device's critical section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6023a211-f493-4d2d-b9ff-1208c44d0d8f">SetMultithreadProtected</a>
</td>
<td align="left" width="63%">
Turn multithreading on or off.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by querying it from the <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a> using <a href="http://msdn.microsoft.com/en-us/library/ms682521(VS.85).aspx">IUnknown::QueryInterface</a>.




## -see-also




<a href="https://msdn.microsoft.com/f5ad2db8-da90-4bcd-83a7-7466723a9c3c">Core Interfaces</a>
 

 

