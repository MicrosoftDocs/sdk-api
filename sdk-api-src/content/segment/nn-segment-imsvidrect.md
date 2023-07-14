---
UID: NN:segment.IMSVidRect
title: IMSVidRect (segment.h)
description: The IMSVidRect interface represents a rectangle with an associated window handle.
helpviewer_keywords: ["IMSVidRect","IMSVidRect interface [Microsoft TV Technologies]","IMSVidRect interface [Microsoft TV Technologies]","described","IMSVidRectInterface","mstv.imsvidrect","segment/IMSVidRect"]
old-location: mstv\imsvidrect.htm
tech.root: mstv
ms.assetid: 0b3cf31b-e0cc-4208-a128-b77460fc0f1b
ms.date: 12/05/2018
ms.keywords: IMSVidRect, IMSVidRect interface [Microsoft TV Technologies], IMSVidRect interface [Microsoft TV Technologies],described, IMSVidRectInterface, mstv.imsvidrect, segment/IMSVidRect
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
 - IMSVidRect
 - segment/IMSVidRect
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
 - IMSVidRect
---

# IMSVidRect interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMSVidRect</b> interface represents a rectangle with an associated window handle. It contains methods to set and retrieve the top and left coordinates, the width, and the height. All values are in pixels. The top and left coordinates are relative to the associated window.

## -inheritance

The <b>IMSVidRect</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMSVidRect</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidRect)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
