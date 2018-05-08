---
UID: NN:d3d12sdklayers.ID3D12DebugDevice
title: ID3D12DebugDevice
author: windows-driver-content
description: This interface represents a graphics device for debugging.
old-location: direct3d12\id3d12debugdevice.htm
old-project: direct3d12
ms.assetid: 6FD77F14-E260-4DBB-8434-664DE1F6DE39
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: ID3D12DebugDevice, ID3D12DebugDevice interface, ID3D12DebugDevice interface,described, d3d12sdklayers/ID3D12DebugDevice, direct3d12.id3d12debugdevice
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
req.typenames: D3D12_RLDO_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d12sdklayers.h
api_name:
-	ID3D12DebugDevice
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12DebugDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12DebugDevice</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/E4ECE63F-6738-4856-9912-93C3AAEE7E3B">GetFeatureMask</a>
</td>
<td align="left" width="63%">

          Gets a bit field of flags that indicates which debug features are on or off.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37771598-DC2E-42FA-B17D-A187164A3314">ReportLiveDeviceObjects</a>
</td>
<td align="left" width="63%">

          Reports information about a device object's lifetime.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12232AB8-BBEA-4663-BEB2-7E296851FE5E">SetFeatureMask</a>
</td>
<td align="left" width="63%">

          Set a bit field of flags that will turn debug features on and off.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9BD5910A-8FF2-4540-BB8E-8EA5C10528CE">Debug Layer Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

