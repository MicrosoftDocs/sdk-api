---
UID: NN:segment.IMSVidEVREvent
title: IMSVidEVREvent (segment.h)
description: This topic applies to Windows Vista or later.helpviewer_keywords: ["IMSVidEVREvent","IMSVidEVREvent interface [Microsoft TV Technologies]","IMSVidEVREvent interface [Microsoft TV Technologies]","described","IMSVidEVREventInterface","mstv.imsvidevrevent","segment/IMSVidEVREvent"]
old-location: mstv\imsvidevrevent.htm
tech.root: mstv
ms.assetid: 70874420-64f2-43c9-b46b-492318ae0852
ms.date: 12/05/2018
ms.keywords: IMSVidEVREvent, IMSVidEVREvent interface [Microsoft TV Technologies], IMSVidEVREvent interface [Microsoft TV Technologies],described, IMSVidEVREventInterface, mstv.imsvidevrevent, segment/IMSVidEVREvent
f1_keywords:
- segment/IMSVidEVREvent
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidEVREvent interface


## -description



This topic applies to Windows Vista or later.
        

The <b>IMSVidEVREvent</b> interface is used to receive events from the Enhanced Video Renderer (EVR) filter.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection. Then call the <b>IConnectionPoint::Advise</b> method on the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695124(v=vs.85)">MSVidEVR</a> object to establish a connection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidEVREvent</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/segment/nn-segment-imsvidoutputdeviceevent">IMSVidOutputDeviceEvent</a>. <b>IMSVidEVREvent</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidevrevent-onuserevent">OnUserEvent</a>
</td>
<td align="left" width="63%">
Forwards custom events from the enhanced video renderer (EVR) filter.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidEVREvent)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/segment/nn-segment-imsvidoutputdeviceevent">IMSVidOutputDeviceEvent</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
 

 

