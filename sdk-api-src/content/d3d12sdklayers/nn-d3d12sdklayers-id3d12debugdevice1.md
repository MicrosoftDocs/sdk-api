---
UID: NN:d3d12sdklayers.ID3D12DebugDevice1
title: ID3D12DebugDevice1
author: windows-sdk-content
description: Specifies device-wide debug layer settings.
old-location: direct3d12\id3d12debugdevice1.htm
tech.root: direct3d12
ms.assetid: DDB71272-195A-4E05-BA52-9EF858ACD6CB
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D12DebugDevice1, ID3D12DebugDevice1 interface, ID3D12DebugDevice1 interface,described, d3d12sdklayers/ID3D12DebugDevice1, direct3d12.id3d12debugdevice1
ms.prod: windows-hardware
ms.technology: windows-devices
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12DebugDevice1</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ID3D12DebugDevice1</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Mt762992(v=VS.85).aspx">GetDebugParameter</a>
</td>
<td align="left" width="63%">
Gets optional device-wide Debug Layer settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt762993(v=VS.85).aspx">ReportLiveDeviceObjects</a>
</td>
<td align="left" width="63%">
Specifies the amount of information to report  on a device object's lifetime.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt762994(v=VS.85).aspx">SetDebugParameter</a>
</td>
<td align="left" width="63%">
Modifies the D3D12 optional device-wide Debug Layer settings.

</td>
</tr>
</table> 


## -remarks



This interface is currently in Preview mode.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn950150(v=VS.85).aspx">Debug Layer Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt490477(v=VS.85).aspx">Using D3D12 Debug Layer GPU-Based Validation</a>
 

 

