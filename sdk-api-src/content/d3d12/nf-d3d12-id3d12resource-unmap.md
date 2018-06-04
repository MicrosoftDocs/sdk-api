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
 

 

