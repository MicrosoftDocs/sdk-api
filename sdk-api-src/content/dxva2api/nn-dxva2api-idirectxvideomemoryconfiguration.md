---
UID: NN:dxva2api.IDirectXVideoMemoryConfiguration
title: IDirectXVideoMemoryConfiguration
author: windows-sdk-content
description: Sets the type of video memory for uncompressed video surfaces.
old-location: mf\idirectxvideomemoryconfiguration.htm
tech.root: medfound
ms.assetid: cc2a6180-9698-460a-9a0d-1ee9e15f197f
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: IDirectXVideoMemoryConfiguration, IDirectXVideoMemoryConfiguration interface [Media Foundation], IDirectXVideoMemoryConfiguration interface [Media Foundation],described, cc2a6180-9698-460a-9a0d-1ee9e15f197f, dxva2api/IDirectXVideoMemoryConfiguration, mf.idirectxvideomemoryconfiguration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - dxva2api.h
api_name:
 - IDirectXVideoMemoryConfiguration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectXVideoMemoryConfiguration interface


## -description


Sets the type of video memory for uncompressed video surfaces. This interface is used by video decoders and transforms.

The DirectShow enhanced video renderer (EVR) filter exposes this interface as a service on the filter's input pins. To obtain a pointer to this interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> with the service identifier MR_VIDEO_ACCELERATION_SERVICE.

A video decoder can use this interface to enumerate the EVR filter's preferred surface types and then select the surface type. The decoder should then create surfaces of that type to hold the results of the decoding operation.

This interface does not define a way to clear the surface type. In the case of DirectShow, disconnecting two filters invalidates the surface type.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectXVideoMemoryConfiguration</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectXVideoMemoryConfiguration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectXVideoMemoryConfiguration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63311052-f01b-4d77-afac-1cc89166f754">GetAvailableSurfaceTypeByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a supported video surface type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06fe0072-1fe5-491f-b0b7-fc85ca731fe7">SetSurfaceType</a>
</td>
<td align="left" width="63%">
Sets the video surface type.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/40deaddb-bb17-4a34-8294-5c7dc8a8a457">Supporting DXVA 2.0 in DirectShow</a>
 

 

