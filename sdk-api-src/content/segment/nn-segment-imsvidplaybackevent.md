---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMSVidPlaybackEvent interface


## -description



This topic applies to Windows XP or later.
        

The <b>IMSVidPlaybackEvent</b> interface is used to receive events from playback devices, such as the file playback object and the stream buffer source object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidPlaybackEvent</b> interface inherits from <a href="https://msdn.microsoft.com/9f35953a-3fea-4187-ad14-28f2c8dc2716">IMSVidInputDeviceEvent</a>. <b>IMSVidPlaybackEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidPlaybackEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00c73b5e-dc0f-4ffd-930f-e93ce3d1e179">EndOfMedia</a>
</td>
<td align="left" width="63%">
Called when playback has reached the end of the source media.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidPlaybackEvent)</code>.




## -see-also




<a href="https://msdn.microsoft.com/7dd435a1-8cd4-45c5-8250-770b629d3f3b">IMSVidFilePlaybackEvent Interface</a>



<a href="https://msdn.microsoft.com/9f35953a-3fea-4187-ad14-28f2c8dc2716">IMSVidInputDeviceEvent</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Event Interfaces</a>
 

 

