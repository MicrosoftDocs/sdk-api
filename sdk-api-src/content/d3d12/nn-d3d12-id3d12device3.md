---
UID: NN:d3d12.ID3D12Device3
title: ID3D12Device3
author: windows-sdk-content
description: Represents a virtual adapter. This interface extends Id3d12device2 to support the creation of special-purpose diagnostic heaps in system memory that persist even in the event of a GPU-fault or device-removed scenario.
old-location: direct3d12\id3d12device3.htm
tech.root: direct3d12
ms.assetid: 038E546C-4000-401A-8A11-7A83F391676E
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Id3d12device3, Id3d12device3 interface, Id3d12device3 interface,described, d3d12/Id3d12device3, direct3d12.id3d12device3
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
 - Id3d12device3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device3 interface


## -description


Represents a virtual adapter. This interface extends <a href="https://msdn.microsoft.com/86C46FD2-7B1D-4F66-97F7-45F9428C5E1E">Id3d12device2</a> to support the creation of special-purpose diagnostic heaps in system memory that persist even in the event of a GPU-fault or device-removed scenario.
<div class="alert"><b>Note</b>  This interface, introduced in the Windows 10 Fall Creators Update, is the latest version of the <a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a> interface. Applications targeting the Windows 10 Fall Creators Update and later should use this interface instead of earlier versions.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Id3d12device3</b> interface inherits from <a href="https://msdn.microsoft.com/86C46FD2-7B1D-4F66-97F7-45F9428C5E1E">Id3d12device2</a>. <b>Id3d12device3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>Id3d12device3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A9F8D656-C09D-47D5-9D97-3C2A60422E96">EnqueueMakeResident</a>
</td>
<td align="left" width="63%">
Asynchronously makes objects resident for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E2343759-FC36-4638-AE91-F6BF6D0BC3BA">OpenExistingHeapFromAddress</a>
</td>
<td align="left" width="63%">
Creates a special-purpose diagnostic heap in system memory from an address. The created heap can persist even in the event of a GPU-fault or device-removed scenario.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0F4B3FC8-59D6-423E-87FB-154234DC8C9D">OpenExistingHeapFromFileMapping</a>
</td>
<td align="left" width="63%">
Creates a special-purpose diagnostic heap in system memory from a file mapping handle. The created heap can persist even in the event of a GPU-fault or device-removed scenario.

</td>
</tr>
</table> 


## -remarks



Use <a href="https://msdn.microsoft.com/F403D730-CBD4-4AE0-86F6-8CE122E82CB4">D3D12CreateDevice</a> to create a device.




## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>



<a href="https://msdn.microsoft.com/7650C695-3F46-405A-9976-A4A50FFAD567">Id3d12device1</a>



<a href="https://msdn.microsoft.com/86C46FD2-7B1D-4F66-97F7-45F9428C5E1E">Id3d12device2</a>
 

 

