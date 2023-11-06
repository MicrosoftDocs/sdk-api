---
UID: NF:segment.IMSVidRect.put_HWnd
title: IMSVidRect::put_HWnd (segment.h)
description: The put_HWnd method specifies the window associated with the rectangle.
helpviewer_keywords: ["IMSVidRect interface [Microsoft TV Technologies]","put_HWnd method","IMSVidRect.put_HWnd","IMSVidRect::put_HWnd","IMSVidRectput_HWnd","mstv.imsvidrect_put_hwnd","put_HWnd","put_HWnd method [Microsoft TV Technologies]","put_HWnd method [Microsoft TV Technologies]","IMSVidRect interface","segment/IMSVidRect::put_HWnd"]
old-location: mstv\imsvidrect_put_hwnd.htm
tech.root: mstv
ms.assetid: bbc7a6d0-2829-4fdb-89da-5ebb7fc803eb
ms.date: 12/05/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],put_HWnd method, IMSVidRect.put_HWnd, IMSVidRect::put_HWnd, IMSVidRectput_HWnd, mstv.imsvidrect_put_hwnd, put_HWnd, put_HWnd method [Microsoft TV Technologies], put_HWnd method [Microsoft TV Technologies],IMSVidRect interface, segment/IMSVidRect::put_HWnd
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
 - IMSVidRect::put_HWnd
 - segment/IMSVidRect::put_HWnd
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
 - IMSVidRect.put_HWnd
---

# IMSVidRect::put_HWnd


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_HWnd</b> method specifies the window associated with the rectangle.

## -parameters

### -param HWndVal [in]

Specifies the handle to the window.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidrect-get_hwnd">IMSVidRect::get_HWnd</a>