---
UID: NN:d3d12.ID3D12Device2
title: ID3D12Device2
author: windows-driver-content
description: Represents a virtual adapter. This interface extends ID3D12Device1 to create pipeline state objects from pipeline state stream descriptions.
old-location: direct3d12\id3d12device2.htm
old-project: direct3d12
ms.assetid: 86C46FD2-7B1D-4F66-97F7-45F9428C5E1E
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: ID3D12Device2, ID3D12Device2 interface, ID3D12Device2 interface, described, d3d12/ID3D12Device2, direct3d12.id3d12device2
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
req.typenames: D3D_SHADER_MODEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D12.dll
api_name:
-	ID3D12Device2
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device2 interface


## -description


Represents a virtual adapter. This interface extends <a href="https://msdn.microsoft.com/7650C695-3F46-405A-9976-A4A50FFAD567">ID3D12Device1</a> to create pipeline state objects from pipeline state stream descriptions.
<div class="alert"><b>Note</b>  This interface was introduced in Windows 10 Creators Update. Applications targetting Windows 10 Creators Update should use this interface instead of earlier or later versions. Applications targetting an earlier or later version of Windows 10 should use the appropriate version of the <b>ID3D12Device</b> interface.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Device2</b> interface inherits from <a href="https://msdn.microsoft.com/7650C695-3F46-405A-9976-A4A50FFAD567">ID3D12Device1</a>. <b>ID3D12Device2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Device2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90557451-CB7A-4F05-8BDB-B611FE034CBB">CreatePipelineState</a>
</td>
<td align="left" width="63%">
Creates a pipeline state object from a pipeline state stream description.

</td>
</tr>
</table> 


## -remarks



Use <a href="https://msdn.microsoft.com/F403D730-CBD4-4AE0-86F6-8CE122E82CB4">D3D12CreateDevice</a> to create a device.




## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>



<a href="https://msdn.microsoft.com/7650C695-3F46-405A-9976-A4A50FFAD567">ID3D12Device1</a>
 

 

