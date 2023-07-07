---
UID: NF:segment.IMSVidRect.put_Rect
title: IMSVidRect::put_Rect (segment.h)
description: The put_Rect method copies the values of another rectangle to this rectangle.
helpviewer_keywords: ["IMSVidRect interface [Microsoft TV Technologies]","put_Rect method","IMSVidRect.put_Rect","IMSVidRect::put_Rect","IMSVidRectput_Rect","mstv.imsvidrect_put_rect","put_Rect","put_Rect method [Microsoft TV Technologies]","put_Rect method [Microsoft TV Technologies]","IMSVidRect interface","segment/IMSVidRect::put_Rect"]
old-location: mstv\imsvidrect_put_rect.htm
tech.root: mstv
ms.assetid: e50fd657-d913-49f5-b4dd-fb4c0d207417
ms.date: 12/05/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],put_Rect method, IMSVidRect.put_Rect, IMSVidRect::put_Rect, IMSVidRectput_Rect, mstv.imsvidrect_put_rect, put_Rect, put_Rect method [Microsoft TV Technologies], put_Rect method [Microsoft TV Technologies],IMSVidRect interface, segment/IMSVidRect::put_Rect
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
 - IMSVidRect::put_Rect
 - segment/IMSVidRect::put_Rect
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
 - IMSVidRect.put_Rect
---

# IMSVidRect::put_Rect


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Rect</b> method copies the values of another rectangle to this rectangle.

## -parameters

### -param RectVal [in]

Specifies a pointer to the <a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect</a> interface of the rectangle to copy.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect Interface</a>