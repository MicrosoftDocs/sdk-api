---
UID: NN:d3d12.ID3D12Fence
title: ID3D12Fence
author: windows-sdk-content
description: Represents a fence, an object used for synchronization of the CPU and one or more GPUs.
old-location: direct3d12\id3d12fence.htm
tech.root: direct3d12
ms.assetid: 2B388352-EF43-4D1E-851C-A670B4681F0F
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ID3D12Fence, ID3D12Fence interface, ID3D12Fence interface,described, d3d12/ID3D12Fence, direct3d12.id3d12fence
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
 - ID3D12Fence
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Fence interface


## -description


Represents a fence, an object used for synchronization of the CPU and one or more GPUs. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Fence</b> interface inherits from <a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>. <b>ID3D12Fence</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Fence</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2F2DDFC5-8D31-4BCE-B378-610C95D7805F">GetCompletedValue</a>
</td>
<td align="left" width="63%">
Gets the current value of the fence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DBC5A1FD-F3D0-4C9B-965B-1967151093F7">SetEventOnCompletion</a>
</td>
<td align="left" width="63%">
Specifies an event that should be fired when the fence reaches a certain value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8AC955C1-37C9-47F3-B35C-980783C58390">Signal</a>
</td>
<td align="left" width="63%">
Sets the fence to the specified value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B">Fence Based Resource Management</a>



<a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>



<a href="https://msdn.microsoft.com/93903F50-A6CA-41C2-863D-68D645586B4C">Synchronization and Multi-Engine</a>
 

 

