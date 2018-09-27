---
UID: NN:d3d12.ID3D12Resource
title: ID3D12Resource
author: windows-sdk-content
description: Encapsulates a generalized ability of the CPU and GPU to read and write to physical memory, or heaps. It contains abstractions for organizing and manipulating simple arrays of data as well as multidimensional data optimized for shader sampling.
old-location: direct3d12\id3d12resource.htm
tech.root: direct3d12
ms.assetid: AF453D2F-F0FD-4552-A843-84119A829CD5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D12Resource, ID3D12Resource interface, ID3D12Resource interface,described, d3d12/ID3D12Resource, direct3d12.id3d12resource
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Resource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Resource interface


## -description


 Encapsulates a generalized ability of the CPU and GPU to read and write to physical memory, or heaps. It contains abstractions for organizing and manipulating simple arrays of data as well as multidimensional data optimized for shader sampling.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Resource</b> interface inherits from <a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>. <b>ID3D12Resource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Resource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B8D84D69-6B13-4E86-8EF6-A841354B1E5C">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the resource description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1B1A345D-D6BD-4DF1-8F10-A209135283AD">GetGPUVirtualAddress</a>
</td>
<td align="left" width="63%">
This method returns the GPU virtual address of a buffer resource.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7F76986D-02F1-4E5A-B9A4-CFB021B72026">GetHeapProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties of the resource heap, for placed and committed resources.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71E43B63-9C84-4E4B-A43D-92B958C8AAF5">Map</a>
</td>
<td align="left" width="63%">
Gets a CPU pointer to the specified subresource in the resource, but may not disclose the pointer value to applications. <a href="https://msdn.microsoft.com/71E43B63-9C84-4E4B-A43D-92B958C8AAF5">Map</a> also invalidates the CPU cache, when necessary, so that CPU reads to this address reflect any modifications made by the GPU.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A1F61217-A383-49BF-B675-FBC7F6D015DB">ReadFromSubresource</a>
</td>
<td align="left" width="63%">
Uses the CPU to copy data from a subresource, enabling the CPU to read the contents of most textures with undefined layouts.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EB0E3936-47CC-4FDC-BF17-A506AC8E4C15">Unmap</a>
</td>
<td align="left" width="63%">
Invalidates the CPU pointer to the specified subresource in the resource. <a href="https://msdn.microsoft.com/EB0E3936-47CC-4FDC-BF17-A506AC8E4C15">Unmap</a> also flushes the CPU cache, when necessary, so that GPU reads to this address reflect any modifications made by the CPU.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8781E2FE-8D82-41F5-B541-A96DA11CA290">WriteToSubresource</a>
</td>
<td align="left" width="63%">
Uses the CPU to copy data into a subresource, enabling the CPU to modify the contents of most textures with undefined layouts.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>
 

 

