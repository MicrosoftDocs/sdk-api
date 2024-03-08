---
UID: NN:segment.IMSVidPlaybackEvent
title: IMSVidPlaybackEvent (segment.h)
description: This topic applies to Windows XP or later.
helpviewer_keywords: ["IMSVidPlaybackEvent","IMSVidPlaybackEvent interface [Microsoft TV Technologies]","IMSVidPlaybackEvent interface [Microsoft TV Technologies]","described","IMSVidPlaybackEventInterface","mstv.imsvidplaybackevent","segment/IMSVidPlaybackEvent"]
old-location: mstv\imsvidplaybackevent.htm
tech.root: mstv
ms.assetid: 7347601e-e889-4a45-8b94-081678df68d9
ms.date: 12/05/2018
ms.keywords: IMSVidPlaybackEvent, IMSVidPlaybackEvent interface [Microsoft TV Technologies], IMSVidPlaybackEvent interface [Microsoft TV Technologies],described, IMSVidPlaybackEventInterface, mstv.imsvidplaybackevent, segment/IMSVidPlaybackEvent
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
 - IMSVidPlaybackEvent
 - segment/IMSVidPlaybackEvent
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
 - IMSVidPlaybackEvent
---

# IMSVidPlaybackEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP or later.
        

The <b>IMSVidPlaybackEvent</b> interface is used to receive events from playback devices, such as the file playback object and the stream buffer source object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.

## -inheritance

The <b>IMSVidPlaybackEvent</b> interface inherits from <a href="/previous-versions/windows/desktop/api/segment/nn-segment-imsvidinputdeviceevent">IMSVidInputDeviceEvent</a>. <b>IMSVidPlaybackEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidPlaybackEvent)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/segment/nn-segment-imsvidfileplaybackevent">IMSVidFilePlaybackEvent Interface</a>



<a href="/previous-versions/windows/desktop/api/segment/nn-segment-imsvidinputdeviceevent">IMSVidInputDeviceEvent</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
