---
UID: NN:d3d12.ID3D12Heap
title: ID3D12Heap
author: windows-sdk-content
description: A heap is an abstraction of contiguous memory allocation, used to manage physical memory. This heap can be used with ID3D12Resource objects to support placed resources or reserved resources.
old-location: direct3d12\id3d12heap.htm
old-project: direct3d12
ms.assetid: 3791C64F-76D7-4580-A444-F2CEA3EB10CE
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: ID3D12Heap, ID3D12Heap interface, ID3D12Heap interface,described, d3d12/ID3D12Heap, direct3d12.id3d12heap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d12.h
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
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Heap
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Heap interface


## -description


A heap  is an abstraction of contiguous memory allocation, used to manage physical memory. This heap can be used with <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a> objects to support placed resources or reserved resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Heap</b> interface inherits from <a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>. <b>ID3D12Heap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Heap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45237F32-FBDE-49FF-926F-80B914B36AE5">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the heap description.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>



<a href="https://msdn.microsoft.com/94D47EBB-8060-49F6-A1FF-8B7B98AD5363">Memory Management in Direct3D 12</a>
 

 

