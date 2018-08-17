---
UID: NN:d3d12sdklayers.ID3D12DebugDevice
title: ID3D12DebugDevice
author: windows-sdk-content
description: This interface represents a graphics device for debugging.
old-location: direct3d12\id3d12debugdevice.htm
old-project: direct3d12
ms.assetid: 6FD77F14-E260-4DBB-8434-664DE1F6DE39
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ID3D12DebugDevice, ID3D12DebugDevice interface, ID3D12DebugDevice interface,described, d3d12sdklayers/ID3D12DebugDevice, direct3d12.id3d12debugdevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d12sdklayers.h
req.include-header: 
req.redist: 
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
req.typenames: D3D12_RLDO_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12DebugDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12DebugDevice interface


## -description


This interface represents a graphics device for debugging.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12DebugDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ID3D12DebugDevice</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D12DebugDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn986874(v=VS.85).aspx">GetFeatureMask</a>
</td>
<td align="left" width="63%">
Gets a bit field of flags that indicates which debug features are on or off.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn986875(v=VS.85).aspx">ReportLiveDeviceObjects</a>
</td>
<td align="left" width="63%">
Reports information about a device object's lifetime.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn986876(v=VS.85).aspx">SetFeatureMask</a>
</td>
<td align="left" width="63%">
Set a bit field of flags that will turn debug features on and off.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn950150(v=VS.85).aspx">Debug Layer Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

