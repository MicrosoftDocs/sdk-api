---
UID: NF:segment.IMSVidVideoRendererEvent.OverlayUnavailable
title: IMSVidVideoRendererEvent::OverlayUnavailable (segment.h)
description: This topic applies to Windows XP or later.
helpviewer_keywords: ["IMSVidVideoRendererEvent interface [Microsoft TV Technologies]","OverlayUnavailable method","IMSVidVideoRendererEvent.OverlayUnavailable","IMSVidVideoRendererEvent::OverlayUnavailable","IMSVidVideoRendererEventOverlayUnavailable","OverlayUnavailable","OverlayUnavailable method [Microsoft TV Technologies]","OverlayUnavailable method [Microsoft TV Technologies]","IMSVidVideoRendererEvent interface","mstv.imsvidvideorendererevent_overlayunavailable","segment/IMSVidVideoRendererEvent::OverlayUnavailable"]
old-location: mstv\imsvidvideorendererevent_overlayunavailable.htm
tech.root: mstv
ms.assetid: cb58e84f-1a45-4b72-aafd-d7a80a4b5b9d
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRendererEvent interface [Microsoft TV Technologies],OverlayUnavailable method, IMSVidVideoRendererEvent.OverlayUnavailable, IMSVidVideoRendererEvent::OverlayUnavailable, IMSVidVideoRendererEventOverlayUnavailable, OverlayUnavailable, OverlayUnavailable method [Microsoft TV Technologies], OverlayUnavailable method [Microsoft TV Technologies],IMSVidVideoRendererEvent interface, mstv.imsvidvideorendererevent_overlayunavailable, segment/IMSVidVideoRendererEvent::OverlayUnavailable
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
 - IMSVidVideoRendererEvent::OverlayUnavailable
 - segment/IMSVidVideoRendererEvent::OverlayUnavailable
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
 - IMSVidVideoRendererEvent.OverlayUnavailable
---

# IMSVidVideoRendererEvent::OverlayUnavailable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP or later.
        



The <b>OverlayUnavailable</b> method is called when the overlay surface on the graphics card is not available.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The dispatch identifier (dispid) of this method is <b>eventidOverlayUnavailable</b>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidvideorendererevent">IMSVidVideoRendererEvent Interface</a>
