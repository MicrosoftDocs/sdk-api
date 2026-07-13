---
UID: NN:segment.IMSVidVideoRendererEvent
title: IMSVidVideoRendererEvent (segment.h)
description: This topic applies to Windows XP or later.
helpviewer_keywords: ["IMSVidVideoRendererEvent","IMSVidVideoRendererEvent interface [Microsoft TV Technologies]","IMSVidVideoRendererEvent interface [Microsoft TV Technologies]","described","IMSVidVideoRendererEventInterface","mstv.imsvidvideorendererevent","segment/IMSVidVideoRendererEvent"]
old-location: mstv\imsvidvideorendererevent.htm
tech.root: mstv
ms.assetid: ff451fa3-a755-4969-bccc-3a014865e7a9
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRendererEvent, IMSVidVideoRendererEvent interface [Microsoft TV Technologies], IMSVidVideoRendererEvent interface [Microsoft TV Technologies],described, IMSVidVideoRendererEventInterface, mstv.imsvidvideorendererevent, segment/IMSVidVideoRendererEvent
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
 - IMSVidVideoRendererEvent
 - segment/IMSVidVideoRendererEvent
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
 - IMSVidVideoRendererEvent
---

# IMSVidVideoRendererEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP or later.
        

The <b>IMSVidVideoRendererEvent</b> interface is used to receive events from the video renderer.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface in your application. Then call the <b>IConnectionPoint::Advise</b> method on the <a href="/previous-versions/windows/desktop/legacy/dd695138(v=vs.85)">MSVidVideoRenderer</a> object to establish a connection.

## -inheritance

The <b>IMSVidVideoRendererEvent</b> interface inherits from <a href="/windows/desktop/api/segment/nn-segment-imsviddeviceevent">IMSVidDeviceEvent</a>. <b>IMSVidVideoRendererEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidVideoRendererEvent)</code>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsviddeviceevent">IMSVidDeviceEvent</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
