---
UID: NF:segment.IMSVidRect.get_Height
title: IMSVidRect::get_Height (segment.h)
description: The get_Height method retrieves the height of the rectangle.
helpviewer_keywords: ["IMSVidRect interface [Microsoft TV Technologies]","get_Height method","IMSVidRect.get_Height","IMSVidRect::get_Height","IMSVidRectget_Height","get_Height","get_Height method [Microsoft TV Technologies]","get_Height method [Microsoft TV Technologies]","IMSVidRect interface","mstv.imsvidrect_get_height","segment/IMSVidRect::get_Height"]
old-location: mstv\imsvidrect_get_height.htm
tech.root: mstv
ms.assetid: 83925bca-8cb2-4f79-9aca-1bee0fb4a96a
ms.date: 12/05/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],get_Height method, IMSVidRect.get_Height, IMSVidRect::get_Height, IMSVidRectget_Height, get_Height, get_Height method [Microsoft TV Technologies], get_Height method [Microsoft TV Technologies],IMSVidRect interface, mstv.imsvidrect_get_height, segment/IMSVidRect::get_Height
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
 - IMSVidRect::get_Height
 - segment/IMSVidRect::get_Height
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
 - IMSVidRect.get_Height
---

# IMSVidRect::get_Height


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Height</b> method retrieves the height of the rectangle.

## -parameters

### -param HeightVal [out]

Pointer to a variable that receives the height, in pixels.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Calling the <a href="/windows/desktop/api/segment/nf-segment-imsvidrect-put_top">IMSVidRect::put_Top</a> method changes the height of the rectangle. For example, if the y-coordinate is zero and the height is 100, setting the y-coordinate to 10 changes the height to 90.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidrect-put_height">IMSVidRect::put_Height</a>