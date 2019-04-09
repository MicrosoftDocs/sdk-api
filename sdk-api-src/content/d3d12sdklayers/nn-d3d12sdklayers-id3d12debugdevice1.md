---
UID: NN:d3d12sdklayers.ID3D12DebugDevice1
title: ID3D12DebugDevice1 (d3d12sdklayers.h)
author: windows-sdk-content
description: Specifies device-wide debug layer settings.
old-location: direct3d12\id3d12debugdevice1.htm
tech.root: direct3d12
ms.assetid: DDB71272-195A-4E05-BA52-9EF858ACD6CB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12DebugDevice1, ID3D12DebugDevice1 interface, ID3D12DebugDevice1 interface,described, d3d12sdklayers/ID3D12DebugDevice1, direct3d12.id3d12debugdevice1
ms.topic: interface
req.header: d3d12sdklayers.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12DebugDevice1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12DebugDevice1 interface


## -description


Specifies device-wide debug layer settings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12DebugDevice1</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12DebugDevice1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12DebugDevice1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13A7E7D6-FF00-4E17-A7C5-C383F93F6A06">GetDebugParameter</a>
</td>
<td align="left" width="63%">
Gets optional device-wide Debug Layer settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99895407-2BFF-40AA-BAE4-C304295DA0E4">ReportLiveDeviceObjects</a>
</td>
<td align="left" width="63%">
Specifies the amount of information to report  on a device object's lifetime.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D97086C6-CED8-4C4E-ADA1-7A172B3202F3">SetDebugParameter</a>
</td>
<td align="left" width="63%">
Modifies the D3D12 optional device-wide Debug Layer settings.

</td>
</tr>
</table> 


## -remarks



This interface is currently in Preview mode.




## -see-also




<a href="https://msdn.microsoft.com/9BD5910A-8FF2-4540-BB8E-8EA5C10528CE">Debug Layer Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/01D1F94F-4DD4-4781-86EF-6C639E8B1069">Using D3D12 Debug Layer GPU-Based Validation</a>
 

 

