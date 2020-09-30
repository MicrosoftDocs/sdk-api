---
UID: NF:segment.IMSVidRect.get_Left
title: IMSVidRect::get_Left (segment.h)
description: The get_Left method retrieves the left x-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.
helpviewer_keywords: ["IMSVidRect interface [Microsoft TV Technologies]","get_Left method","IMSVidRect.get_Left","IMSVidRect::get_Left","IMSVidRectget_Left","get_Left","get_Left method [Microsoft TV Technologies]","get_Left method [Microsoft TV Technologies]","IMSVidRect interface","mstv.imsvidrect_get_left","segment/IMSVidRect::get_Left"]
old-location: mstv\imsvidrect_get_left.htm
tech.root: mstv
ms.assetid: 9e64e560-033b-475a-a281-57af5f893e65
ms.date: 12/05/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],get_Left method, IMSVidRect.get_Left, IMSVidRect::get_Left, IMSVidRectget_Left, get_Left, get_Left method [Microsoft TV Technologies], get_Left method [Microsoft TV Technologies],IMSVidRect interface, mstv.imsvidrect_get_left, segment/IMSVidRect::get_Left
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
 - IMSVidRect::get_Left
 - segment/IMSVidRect::get_Left
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
 - IMSVidRect.get_Left
---

# IMSVidRect::get_Left


## -description

The <b>get_Left</b> method retrieves the left x-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.

## -parameters

### -param LeftVal [out]

Pointer to a variable that receives the left x-coordinate, in pixels.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidrect-get_hwnd">IMSVidRect::get_HWnd</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidrect-put_left">IMSVidRect::put_Left</a>