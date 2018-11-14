---
UID: NN:d3d12.ID3D12DeviceChild
title: ID3D12DeviceChild
author: windows-sdk-content
description: An interface from which other core interfaces inherit from, including ID3D12PipelineLibrary, ID3D12CommandList, ID3D12Pageable, and ID3D12RootSignature. It provides a method to get back to the device object it was created against.
old-location: direct3d12\id3d12devicechild.htm
tech.root: direct3d12
ms.assetid: AED60281-A6E4-4AAD-A106-6CA6E9BAEB9A
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID3D12DeviceChild, ID3D12DeviceChild interface, ID3D12DeviceChild interface,described, d3d12/ID3D12DeviceChild, direct3d12.id3d12devicechild
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D12DeviceChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12DeviceChild interface


## -description


An interface from which other core interfaces inherit from, including <a href="https://msdn.microsoft.com/7A1D750D-51F1-48F6-9D74-6439A147F1EC">ID3D12PipelineLibrary</a>,  <a href="https://msdn.microsoft.com/1E0359CC-0F53-4C82-9F1A-092F6F72EE20">ID3D12CommandList</a>, <a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>, and <a href="https://msdn.microsoft.com/BEE01381-12C2-4DD9-9121-22BB5840ECD5">ID3D12RootSignature</a>. It provides a method to get back to the device object it was created against.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12DeviceChild</b> interface inherits from <a href="https://msdn.microsoft.com/D2B2BC74-E89D-4D3A-8808-6E4A94992769">ID3D12Object</a>. <b>ID3D12DeviceChild</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12DeviceChild</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FFF72E85-4382-420B-82C9-CE72B223F703">GetDevice</a>
</td>
<td align="left" width="63%">
Gets a pointer to the device that created this interface. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/D2B2BC74-E89D-4D3A-8808-6E4A94992769">ID3D12Object</a>
 

 

