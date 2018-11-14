---
UID: NN:d3d11_3.ID3D11Fence
title: ID3D11Fence
author: windows-sdk-content
description: Represents a fence, an object used for synchronization of the CPU and one or more GPUs.
old-location: direct3d11\id3d11fence.htm
tech.root: direct3d11
ms.assetid: DC07EDEF-DA38-4CAF-8FDE-B3867DC83B8C
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11Fence, ID3D11Fence interface [Direct3D 11], ID3D11Fence interface [Direct3D 11],described, d3d11_3/ID3D11Fence, direct3d11.id3d11fence
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d11_3.h
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
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.dll
api_name:
 - ID3D11Fence
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Fence interface


## -description


Represents a fence, an object used for synchronization of the CPU and one or more GPUs.

This interface is equivalent to the Direct3D 12 <a href="https://msdn.microsoft.com/en-us/library/Dn899188(v=VS.85).aspx">ID3D12Fence</a> inteface, and is also used for synchronization between Direct3D 11 and Direct3D 12 in interop scenarios.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Fence</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>. <b>ID3D11Fence</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11Fence</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt492485(v=VS.85).aspx">CreateSharedHandle</a>
</td>
<td align="left" width="63%">
Creates a shared handle to a fence object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt492486(v=VS.85).aspx">GetCompletedValue</a>
</td>
<td align="left" width="63%">
Gets the current value of the fence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt492487(v=VS.85).aspx">SetEventOnCompletion</a>
</td>
<td align="left" width="63%">
Specifies an event that should be fired when the fence reaches a certain value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476154(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn899125(v=VS.85).aspx">Fence Based Resource Management (Direct3D 12)</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn899217(v=VS.85).aspx">Synchronization and Multi-Engine (Direct3D 12)</a>
 

 

