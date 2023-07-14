---
UID: NF:segment.IMSVidRect.get_HWnd
title: IMSVidRect::get_HWnd (segment.h)
description: The get_HWnd method retrieves the window associated with the rectangle.
helpviewer_keywords: ["IMSVidRect interface [Microsoft TV Technologies]","get_HWnd method","IMSVidRect.get_HWnd","IMSVidRect::get_HWnd","IMSVidRectget_HWnd","get_HWnd","get_HWnd method [Microsoft TV Technologies]","get_HWnd method [Microsoft TV Technologies]","IMSVidRect interface","mstv.imsvidrect_get_hwnd","segment/IMSVidRect::get_HWnd"]
old-location: mstv\imsvidrect_get_hwnd.htm
tech.root: mstv
ms.assetid: caa56beb-7eba-48a1-8645-f63666ba0593
ms.date: 12/05/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],get_HWnd method, IMSVidRect.get_HWnd, IMSVidRect::get_HWnd, IMSVidRectget_HWnd, get_HWnd, get_HWnd method [Microsoft TV Technologies], get_HWnd method [Microsoft TV Technologies],IMSVidRect interface, mstv.imsvidrect_get_hwnd, segment/IMSVidRect::get_HWnd
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
 - IMSVidRect::get_HWnd
 - segment/IMSVidRect::get_HWnd
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
 - IMSVidRect.get_HWnd
---

# IMSVidRect::get_HWnd


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_HWnd</b> method retrieves the window associated with the rectangle.

## -parameters

### -param HWndVal [out]

Pointer to a variable that receives a handle to the window.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidrect-put_hwnd">IMSVidRect::put_HWnd</a>