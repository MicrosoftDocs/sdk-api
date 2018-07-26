---
UID: NN:d3d12.ID3D12Device1
title: ID3D12Device1
author: windows-sdk-content
description: Represents a virtual adapter, and expands on the range of methods provided by ID3D12Device.
old-location: direct3d12\id3d12device1.htm
old-project: direct3d12
ms.assetid: 7650C695-3F46-405A-9976-A4A50FFAD567
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ID3D12Device1, ID3D12Device1 interface, ID3D12Device1 interface,described, d3d12/ID3D12Device1, direct3d12.id3d12device1
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
 - d3d12.dll
api_name:
 - ID3D12Device1
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12Device1 interface


## -description


Represents a virtual adapter, and expands on the range of methods provided by <a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>.
<div class="alert"><b>Note</b>  This interface was introduced in Windows 10 Anniversary Update. Applications targetting Windows 10 Anniversary Update should use this interface instead of earlier or later versions. Applications targetting an earlier or later version of Windows 10 should use the appropriate version of the <b>ID3D12Device</b> interface.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Device1</b> interface inherits from <a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>. <b>ID3D12Device1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Device1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/572A95A6-A02F-4512-9BDE-2A8CA58A0A27">CreatePipelineLibrary</a>
</td>
<td align="left" width="63%">
Creates a cached pipeline library. By grouping PSOs that are expected to share data together into a library before serializing, there’s less overhead due to metadata, as well as opportunity to avoid redundant or duplicated data from being written to disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C187EEB7-DCD0-4535-AF0E-EF2C0E2DC83C">SetEventOnMultipleFenceCompletion</a>
</td>
<td align="left" width="63%">
Specifies an event that should be fired when one or more of a collection of fences reach specific values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C489AA41-B2FC-418D-8268-9C02E5E10E0D">SetResidencyPriority</a>
</td>
<td align="left" width="63%">
This method sets residency priorities of a specified list of objects.

</td>
</tr>
</table> 


## -remarks



Use <a href="https://msdn.microsoft.com/F403D730-CBD4-4AE0-86F6-8CE122E82CB4">D3D12CreateDevice</a> to create a device. 




## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>



<a href="https://msdn.microsoft.com/86C46FD2-7B1D-4F66-97F7-45F9428C5E1E">ID3D12Device2</a>
 

 

