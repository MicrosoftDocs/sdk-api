---
UID: NN:d3d10.ID3D10Multithread
title: ID3D10Multithread
author: windows-sdk-content
description: A multithread interface accesses multithread settings and can only be used if the thread-safe layer is turned on.
old-location: direct3d10\id3d10multithread.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10multithread.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 03af3cb4-f8ff-e677-80ea-33ee09667866, ID3D10Multithread, ID3D10Multithread interface [Direct3D 10], ID3D10Multithread interface [Direct3D 10],described, d3d10/ID3D10Multithread, direct3d10.id3d10multithread
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
 - ID3D10Multithread
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Multithread interface


## -description


A multithread interface accesses multithread settings and can only be used if the <a href="https://msdn.microsoft.com/en-us/library/Bb205068(v=VS.85).aspx">thread-safe layer</a> is turned on. 


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
<a href="https://msdn.microsoft.com/en-us/library/Bb173817(v=VS.85).aspx">Enter</a>
</td>
<td align="left" width="63%">
Enter a device's critical section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173818(v=VS.85).aspx">GetMultithreadProtected</a>
</td>
<td align="left" width="63%">
Find out if multithreading is turned on or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173819(v=VS.85).aspx">Leave</a>
</td>
<td align="left" width="63%">
Leave a device's critical section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173820(v=VS.85).aspx">SetMultithreadProtected</a>
</td>
<td align="left" width="63%">
Turn multithreading on or off.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by querying it from the <a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a> using <a href="http://msdn.microsoft.com/en-us/library/ms682521(VS.85).aspx">IUnknown::QueryInterface</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205152(v=VS.85).aspx">Core Interfaces</a>
 

 

