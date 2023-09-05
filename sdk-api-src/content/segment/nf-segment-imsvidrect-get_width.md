---
UID: NF:segment.IMSVidRect.get_Width
title: IMSVidRect::get_Width (segment.h)
description: The get_Width method retrieves the width of the rectangle.
helpviewer_keywords: ["IMSVidRect interface [Microsoft TV Technologies]","get_Width method","IMSVidRect.get_Width","IMSVidRect::get_Width","IMSVidRectget_Width","get_Width","get_Width method [Microsoft TV Technologies]","get_Width method [Microsoft TV Technologies]","IMSVidRect interface","mstv.imsvidrect_get_width","segment/IMSVidRect::get_Width"]
old-location: mstv\imsvidrect_get_width.htm
tech.root: mstv
ms.assetid: 7b1d07b8-41e4-44f8-8c28-377c7a9e463d
ms.date: 12/05/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],get_Width method, IMSVidRect.get_Width, IMSVidRect::get_Width, IMSVidRectget_Width, get_Width, get_Width method [Microsoft TV Technologies], get_Width method [Microsoft TV Technologies],IMSVidRect interface, mstv.imsvidrect_get_width, segment/IMSVidRect::get_Width
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
 - IMSVidRect::get_Width
 - segment/IMSVidRect::get_Width
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
 - IMSVidRect.get_Width
---

# IMSVidRect::get_Width


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Width</b> method retrieves the width of the rectangle.

## -parameters

### -param WidthVal [out]

Pointer to a variable that receives the width, in pixels.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Calling the <a href="/windows/desktop/api/segment/nf-segment-imsvidrect-put_left">IMSVidRect::put_Left</a> method changes the width of the rectangle. For example, if the x-coordinate is zero and the width is 100, setting the x-coordinate to 10 changes the width to 90.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidrect-put_width">IMSVidRect::put_Width</a>