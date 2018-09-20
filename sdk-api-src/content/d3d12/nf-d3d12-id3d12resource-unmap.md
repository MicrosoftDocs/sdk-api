---
UID: NF:d3d12.ID3D12Resource.Unmap
title: ID3D12Resource::Unmap
author: windows-sdk-content
description: Invalidates the CPU pointer to the specified subresource in the resource. Unmap also flushes the CPU cache, when necessary, so that GPU reads to this address reflect any modifications made by the CPU.
old-location: direct3d12\id3d12resource_unmap.htm
tech.root: direct3d12
ms.assetid: EB0E3936-47CC-4FDC-BF17-A506AC8E4C15
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ID3D12Resource interface,Unmap method, ID3D12Resource.Unmap, ID3D12Resource::Unmap, Unmap, Unmap method, Unmap method,ID3D12Resource interface, d3d12/ID3D12Resource::Unmap, direct3d12.id3d12resource_unmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID3D12Resource.Unmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Resource::Unmap


## -description


Invalidates the CPU pointer to the specified subresource in the resource. <b>Unmap</b> also flushes the CPU cache, when necessary, so that GPU reads to this address reflect any modifications made by the CPU.



## -parameters




### -param Subresource

Type: <b>UINT</b>

Specifies the index of the subresource.


### -param pWrittenRange [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/E8A66EC7-DB20-475D-BCD1-6C164FF39D24">D3D12_RANGE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/E8A66EC7-DB20-475D-BCD1-6C164FF39D24">D3D12_RANGE</a> structure that describes the range of memory to unmap.

This indicates the region the CPU might have modified, and the coordinates are subresource-relative. A null pointer indicates the entire subresource might have been modified by the CPU. It is valid to specify the CPU didn't write any data by passing a range where <b>End</b> is less than or equal to <b>Begin</b>.


## -returns



This method does not return a value.




## -remarks



Refer to the extensive Remarks and Examples for the <a href="https://msdn.microsoft.com/71E43B63-9C84-4E4B-A43D-92B958C8AAF5">Map</a> method.




## -see-also




<a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>



<a href="https://msdn.microsoft.com/71E43B63-9C84-4E4B-A43D-92B958C8AAF5">Map</a>



<a href="https://msdn.microsoft.com/C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F">Subresources</a>
 

 

