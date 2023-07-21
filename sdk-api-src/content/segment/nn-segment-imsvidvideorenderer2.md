---
UID: NN:segment.IMSVidVideoRenderer2
title: IMSVidVideoRenderer2 (segment.h)
description: The IMSVidVideoRenderer2 interface represents a video renderer device.
helpviewer_keywords: ["IMSVidVideoRenderer2","IMSVidVideoRenderer2 interface [Microsoft TV Technologies]","IMSVidVideoRenderer2 interface [Microsoft TV Technologies]","described","IMSVidVideoRenderer2Interface","mstv.imsvidvideorenderer2","segment/IMSVidVideoRenderer2"]
old-location: mstv\imsvidvideorenderer2.htm
tech.root: mstv
ms.assetid: caaa2cf1-15be-47dc-82db-06915a55ba03
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer2, IMSVidVideoRenderer2 interface [Microsoft TV Technologies], IMSVidVideoRenderer2 interface [Microsoft TV Technologies],described, IMSVidVideoRenderer2Interface, mstv.imsvidvideorenderer2, segment/IMSVidVideoRenderer2
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IMSVidVideoRenderer2
 - segment/IMSVidVideoRenderer2
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
 - IMSVidVideoRenderer2
---

# IMSVidVideoRenderer2 interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMSVidVideoRenderer2</b> interface represents a video renderer device. The <a href="/previous-versions/windows/desktop/legacy/dd695138(v=vs.85)">MSVidVideoRenderer</a> object exposes this interface.

This interface provides access to the Video Mixing Renderer (VMR) filter. It inherits the <a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer</a> interface and adds support for custom allocator-presenters.

## -inheritance

The <b>IMSVidVideoRenderer2</b> interface inherits from <a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer</a>. <b>IMSVidVideoRenderer2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidVideoRenderer2)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
