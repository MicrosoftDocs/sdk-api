---
UID: NN:segment.IMSVidStreamBufferSourceEvent
title: IMSVidStreamBufferSourceEvent (segment.h)
description: This topic applies to Windows XP Service Pack 1 or later.
helpviewer_keywords: ["IMSVidStreamBufferSourceEvent","IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies]","IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies]","described","IMSVidStreamBufferSourceEventInterface","mstv.imsvidstreambuffersourceevent","segment/IMSVidStreamBufferSourceEvent"]
old-location: mstv\imsvidstreambuffersourceevent.htm
tech.root: mstv
ms.assetid: 6d8e0cf3-b4c7-4f3e-acff-50f12b8340a8
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSourceEvent, IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies], IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies],described, IMSVidStreamBufferSourceEventInterface, mstv.imsvidstreambuffersourceevent, segment/IMSVidStreamBufferSourceEvent
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
 - IMSVidStreamBufferSourceEvent
 - segment/IMSVidStreamBufferSourceEvent
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
 - IMSVidStreamBufferSourceEvent
---

# IMSVidStreamBufferSourceEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP Service Pack 1 or later.
        

The <b>IMSVidStreamBufferSourceEvent</b> interface is used to receive events from the <a href="/previous-versions/windows/desktop/legacy/dd695136(v=vs.85)">MSVidStreamBufferSource</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.

## -inheritance

The <b>IMSVidStreamBufferSourceEvent</b> interface inherits from <a href="/previous-versions/windows/desktop/api/segment/nn-segment-imsvidfileplaybackevent">IMSVidFilePlaybackEvent</a>. <b>IMSVidStreamBufferSourceEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSourceEvent)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/segment/nn-segment-imsvidfileplaybackevent">IMSVidFilePlaybackEvent</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
