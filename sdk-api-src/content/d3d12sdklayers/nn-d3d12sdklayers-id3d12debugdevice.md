---
UID: NN:d3d12sdklayers.ID3D12DebugDevice
title: ID3D12DebugDevice (d3d12sdklayers.h)
description: This interface represents a graphics device for debugging.
old-location: direct3d12\id3d12debugdevice.htm
tech.root: direct3d12
ms.assetid: 6FD77F14-E260-4DBB-8434-664DE1F6DE39
ms.date: 12/05/2018
ms.keywords: ID3D12DebugDevice, ID3D12DebugDevice interface, ID3D12DebugDevice interface,described, d3d12sdklayers/ID3D12DebugDevice, direct3d12.id3d12debugdevice
ms.topic: interface
f1_keywords:
- d3d12sdklayers/ID3D12DebugDevice
dev_langs:
- c++
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
- ID3D12DebugDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12DebugDevice interface


## -description


This interface represents a graphics device for debugging.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12DebugDevice</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12DebugDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice-getfeaturemask">GetFeatureMask</a>
</td>
<td align="left" width="63%">
Gets a bit field of flags that indicates which debug features are on or off.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice-reportlivedeviceobjects">ReportLiveDeviceObjects</a>
</td>
<td align="left" width="63%">
Reports information about a device object's lifetime.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice-setfeaturemask">SetFeatureMask</a>
</td>
<td align="left" width="63%">
Set a bit field of flags that will turn debug features on and off.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-sdklayers-interfaces">Debug Layer Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

