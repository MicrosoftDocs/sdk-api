---
UID: NF:segment.IMSVidRect.put_Left
title: IMSVidRect::put_Left (segment.h)
description: The put_Left method specifies the left x-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.
helpviewer_keywords: ["IMSVidRect interface [Microsoft TV Technologies]","put_Left method","IMSVidRect.put_Left","IMSVidRect::put_Left","IMSVidRectput_Left","mstv.imsvidrect_put_left","put_Left","put_Left method [Microsoft TV Technologies]","put_Left method [Microsoft TV Technologies]","IMSVidRect interface","segment/IMSVidRect::put_Left"]
old-location: mstv\imsvidrect_put_left.htm
tech.root: mstv
ms.assetid: 8e61fd8a-9ea0-48c1-8749-780b0363c12d
ms.date: 12/05/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],put_Left method, IMSVidRect.put_Left, IMSVidRect::put_Left, IMSVidRectput_Left, mstv.imsvidrect_put_left, put_Left, put_Left method [Microsoft TV Technologies], put_Left method [Microsoft TV Technologies],IMSVidRect interface, segment/IMSVidRect::put_Left
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
 - IMSVidRect::put_Left
 - segment/IMSVidRect::put_Left
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
 - IMSVidRect.put_Left
---

# IMSVidRect::put_Left


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Left</b> method specifies the left x-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.

## -parameters

### -param LeftVal [in]

Specifies the left x-coordinate, in pixels.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Setting the left x-coordinate also changes the width of the rectangle. For example, if the x-coordinate is zero and the width is 100, setting the x-coordinate to 10 changes the width to 90.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidrect-get_hwnd">IMSVidRect::get_HWnd</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidrect-get_left">IMSVidRect::get_Left</a>