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

This topic applies to Windows XP or later.
        

The <b>IMSVidVideoRendererEvent</b> interface is used to receive events from the video renderer.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface in your application. Then call the <b>IConnectionPoint::Advise</b> method on the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695138(v=vs.85)">MSVidVideoRenderer</a> object to establish a connection.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidVideoRendererEvent</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsviddeviceevent">IMSVidDeviceEvent</a>. <b>IMSVidVideoRendererEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidVideoRendererEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorendererevent-overlayunavailable">OverlayUnavailable</a>
</td>
<td align="left" width="63%">
Called when the overlay surface on the graphics card is not available.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidVideoRendererEvent)</code>.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsviddeviceevent">IMSVidDeviceEvent</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>

