---
UID: NN:segment.IMSVidDeviceEvent
title: IMSVidDeviceEvent (segment.h)
description: This topic applies to Windows XP or later. The IMSVidDeviceEvent interface is the base interface for device events. Do not implement this interface directly. Other event interfaces derive from this interface.helpviewer_keywords: ["IMSVidDeviceEvent","IMSVidDeviceEvent interface [Microsoft TV Technologies]","IMSVidDeviceEvent interface [Microsoft TV Technologies]","described","IMSVidDeviceEventInterface","mstv.imsviddeviceevent","segment/IMSVidDeviceEvent"]
old-location: mstv\imsviddeviceevent.htm
tech.root: mstv
ms.assetid: 1a5a9bc1-7d18-4aa9-bc5f-318f7bedbc48
ms.date: 12/05/2018
ms.keywords: IMSVidDeviceEvent, IMSVidDeviceEvent interface [Microsoft TV Technologies], IMSVidDeviceEvent interface [Microsoft TV Technologies],described, IMSVidDeviceEventInterface, mstv.imsviddeviceevent, segment/IMSVidDeviceEvent
f1_keywords:
- segment/IMSVidDeviceEvent
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
- IMSVidDeviceEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidDeviceEvent interface


## -description



This topic applies to Windows XP or later.
        

The <b>IMSVidDeviceEvent</b> interface is the base interface for device events. Do not implement this interface directly. Other event interfaces derive from this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidDeviceEvent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMSVidDeviceEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidDeviceEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsviddeviceevent-statechange">StateChange</a>
</td>
<td align="left" width="63%">
Signals that the state of the device has changed.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidDeviceEvent)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
 

 

