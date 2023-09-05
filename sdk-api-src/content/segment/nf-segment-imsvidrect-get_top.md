---
UID: NF:segment.IMSVidRect.get_Top
title: IMSVidRect::get_Top (segment.h)
description: The get_Top method retrieves the top y-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.
helpviewer_keywords: ["IMSVidRect interface [Microsoft TV Technologies]","get_Top method","IMSVidRect.get_Top","IMSVidRect::get_Top","IMSVidRectget_Top","get_Top","get_Top method [Microsoft TV Technologies]","get_Top method [Microsoft TV Technologies]","IMSVidRect interface","mstv.imsvidrect_get_top","segment/IMSVidRect::get_Top"]
old-location: mstv\imsvidrect_get_top.htm
tech.root: mstv
ms.assetid: 3596141c-e359-4ea5-8d6a-9ec374c1f854
ms.date: 12/05/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],get_Top method, IMSVidRect.get_Top, IMSVidRect::get_Top, IMSVidRectget_Top, get_Top, get_Top method [Microsoft TV Technologies], get_Top method [Microsoft TV Technologies],IMSVidRect interface, mstv.imsvidrect_get_top, segment/IMSVidRect::get_Top
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
 - IMSVidRect::get_Top
 - segment/IMSVidRect::get_Top
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
 - IMSVidRect.get_Top
---

# IMSVidRect::get_Top


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Top</b> method retrieves the top y-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.

## -parameters

### -param TopVal [out]

Pointer to a variable that receives the top y-coordinate, in pixels.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidrect-get_hwnd">IMSVidRect::get_HWnd</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidrect-put_top">IMSVidRect::put_Top</a>