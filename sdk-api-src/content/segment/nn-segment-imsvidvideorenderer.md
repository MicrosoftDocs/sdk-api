---
UID: NN:segment.IMSVidVideoRenderer
title: IMSVidVideoRenderer (segment.h)
description: The IMSVidVideoRenderer interface represents a video renderer device. The MSVidVideoRenderer object exposes this interface.This interface provides access to the Video Mixing Renderer (VMR) filter.
helpviewer_keywords: ["IMSVidVideoRenderer","IMSVidVideoRenderer interface [Microsoft TV Technologies]","IMSVidVideoRenderer interface [Microsoft TV Technologies]","described","IMSVidVideoRendererInterface","mstv.imsvidvideorenderer","segment/IMSVidVideoRenderer"]
old-location: mstv\imsvidvideorenderer.htm
tech.root: mstv
ms.assetid: 27eb53f8-ece8-43eb-8f94-b3d2d91548ad
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer, IMSVidVideoRenderer interface [Microsoft TV Technologies], IMSVidVideoRenderer interface [Microsoft TV Technologies],described, IMSVidVideoRendererInterface, mstv.imsvidvideorenderer, segment/IMSVidVideoRenderer
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
 - IMSVidVideoRenderer
 - segment/IMSVidVideoRenderer
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
 - IMSVidVideoRenderer
---

# IMSVidVideoRenderer interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMSVidVideoRenderer</b> interface represents a video renderer device. The <a href="/previous-versions/windows/desktop/legacy/dd695138(v=vs.85)">MSVidVideoRenderer</a> object exposes this interface.

This interface provides access to the Video Mixing Renderer (VMR) filter.

## -inheritance

The <b>IMSVidVideoRenderer</b> interface inherits from <a href="/previous-versions/windows/desktop/mstv/msvidoutputdevice">IMSVidOutputDevice</a>. <b>IMSVidVideoRenderer</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidVideoRenderer)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidoutputdevice">IMSVidOutputDevice</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
