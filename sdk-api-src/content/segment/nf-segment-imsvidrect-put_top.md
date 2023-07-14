---
UID: NF:segment.IMSVidRect.put_Top
title: IMSVidRect::put_Top (segment.h)
description: The put_Top method specifies the top y-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.
helpviewer_keywords: ["IMSVidRect interface [Microsoft TV Technologies]","put_Top method","IMSVidRect.put_Top","IMSVidRect::put_Top","IMSVidRectput_Top","mstv.imsvidrect_put_top","put_Top","put_Top method [Microsoft TV Technologies]","put_Top method [Microsoft TV Technologies]","IMSVidRect interface","segment/IMSVidRect::put_Top"]
old-location: mstv\imsvidrect_put_top.htm
tech.root: mstv
ms.assetid: ee3dbbd2-a8b4-496b-84e6-b0d7615f6a1e
ms.date: 12/05/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],put_Top method, IMSVidRect.put_Top, IMSVidRect::put_Top, IMSVidRectput_Top, mstv.imsvidrect_put_top, put_Top, put_Top method [Microsoft TV Technologies], put_Top method [Microsoft TV Technologies],IMSVidRect interface, segment/IMSVidRect::put_Top
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
 - IMSVidRect::put_Top
 - segment/IMSVidRect::put_Top
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
 - IMSVidRect.put_Top
---

# IMSVidRect::put_Top


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Top</b> method specifies the top y-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.

## -parameters

### -param TopVal [in]

Specifies the top y-coordinate, in pixels.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Setting the top y-coordinate also changes the height of the rectangle. For example, if the y-coordinate is zero and the height is 100, setting the y-coordinate to 10 changes the height to 90.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidrect-get_hwnd">IMSVidRect::get_HWnd</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidrect-get_top">IMSVidRect::get_Top</a>