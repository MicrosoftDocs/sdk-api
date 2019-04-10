---
UID: NN:segment.IMSVidEVREvent
title: IMSVidEVREvent (segment.h)
author: windows-sdk-content
description: This topic applies to Windows Vista or later.
old-location: mstv\imsvidevrevent.htm
tech.root: mstv
ms.assetid: 70874420-64f2-43c9-b46b-492318ae0852
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidEVREvent, IMSVidEVREvent interface [Microsoft TV Technologies], IMSVidEVREvent interface [Microsoft TV Technologies],described, IMSVidEVREventInterface, mstv.imsvidevrevent, segment/IMSVidEVREvent
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - segment.h
api_name:
 - IMSVidEVREvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidEVREvent interface


## -description



This topic applies to Windows Vista or later.
        

The <b>IMSVidEVREvent</b> interface is used to receive events from the Enhanced Video Renderer (EVR) filter.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection. Then call the <b>IConnectionPoint::Advise</b> method on the <a href="https://msdn.microsoft.com/0f22bb13-2246-4933-940e-8380222af355">MSVidEVR</a> object to establish a connection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidEVREvent</b> interface inherits from <a href="https://msdn.microsoft.com/4f3ad7c0-02fd-4232-89f1-49517c23ee28">IMSVidOutputDeviceEvent</a>. <b>IMSVidEVREvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidEVREvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694538(v=VS.85).aspx">OnUserEvent</a>
</td>
<td align="left" width="63%">
Forwards custom events from the enhanced video renderer (EVR) filter.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidEVREvent)</code>.




## -see-also




<a href="https://msdn.microsoft.com/4f3ad7c0-02fd-4232-89f1-49517c23ee28">IMSVidOutputDeviceEvent</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Event Interfaces</a>
 

 

