---
UID: NN:segment.IMSVidStreamBufferSinkEvent
title: IMSVidStreamBufferSinkEvent (segment.h)
description: This topic applies to Windows XP Service Pack 1 or later.
helpviewer_keywords: ["IMSVidStreamBufferSinkEvent","IMSVidStreamBufferSinkEvent interface [Microsoft TV Technologies]","IMSVidStreamBufferSinkEvent interface [Microsoft TV Technologies]","described","IMSVidStreamBufferSinkEventInterface","mstv.imsvidstreambuffersinkevent","segment/IMSVidStreamBufferSinkEvent"]
old-location: mstv\imsvidstreambuffersinkevent.htm
tech.root: mstv
ms.assetid: e828d3e0-5a2a-499a-a718-11aa76a01b1b
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSinkEvent, IMSVidStreamBufferSinkEvent interface [Microsoft TV Technologies], IMSVidStreamBufferSinkEvent interface [Microsoft TV Technologies],described, IMSVidStreamBufferSinkEventInterface, mstv.imsvidstreambuffersinkevent, segment/IMSVidStreamBufferSinkEvent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidStreamBufferSinkEvent
 - segment/IMSVidStreamBufferSinkEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSinkEvent
---

# IMSVidStreamBufferSinkEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP Service Pack 1 or later.
        

The <b>IMSVidStreamBufferSinkEvent</b> interface is used to receive events from the <a href="/previous-versions/windows/desktop/legacy/dd695135(v=vs.85)">MSVidStreamBufferSink</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.

## -inheritance

The <b>IMSVidStreamBufferSinkEvent</b> interface inherits from <a href="/previous-versions/windows/desktop/api/segment/nn-segment-imsvidoutputdeviceevent">IMSVidOutputDeviceEvent</a>. <b>IMSVidStreamBufferSinkEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSinkEvent)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/segment/nn-segment-imsvidoutputdeviceevent">IMSVidOutputDeviceEvent</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
