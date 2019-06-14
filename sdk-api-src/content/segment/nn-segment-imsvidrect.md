---
UID: NN:segment.IMSVidRect
title: IMSVidRect (segment.h)
author: windows-sdk-content
description: The IMSVidRect interface represents a rectangle with an associated window handle.
old-location: mstv\imsvidrect.htm
tech.root: mstv
ms.assetid: 0b3cf31b-e0cc-4208-a128-b77460fc0f1b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidRect, IMSVidRect interface [Microsoft TV Technologies], IMSVidRect interface [Microsoft TV Technologies],described, IMSVidRectInterface, mstv.imsvidrect, segment/IMSVidRect
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidRect interface


## -description



The <b>IMSVidRect</b> interface represents a rectangle with an associated window handle. It contains methods to set and retrieve the top and left coordinates, the width, and the height. All values are in pixels. The top and left coordinates are relative to the associated window.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidRect</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMSVidRect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidRect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidrect-get_height">get_Height</a>
</td>
<td align="left" width="63%">
Retrieves the height of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidrect-get_hwnd">get_HWnd</a>
</td>
<td align="left" width="63%">
Retrieves the window associated with the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidrect-get_left">get_Left</a>
</td>
<td align="left" width="63%">
Retrieves the left x-coordinate of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidrect-get_top">get_Top</a>
</td>
<td align="left" width="63%">
Retrieves the top y-coordinate of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidrect-get_width">get_Width</a>
</td>
<td align="left" width="63%">
Retrieves the width of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidrect-put_height">put_Height</a>
</td>
<td align="left" width="63%">
Specifies the height of the rectangle

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidrect-put_hwnd">put_HWnd</a>
</td>
<td align="left" width="63%">
Specifies the window associated with the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidrect-put_left">put_Left</a>
</td>
<td align="left" width="63%">
Specifies the left x-coordinate of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidrect-put_rect">put_Rect</a>
</td>
<td align="left" width="63%">
Copies the values of another rectangle to this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidrect-put_top">put_Top</a>
</td>
<td align="left" width="63%">
Specifies the top y-coordinate of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidrect-put_width">put_Width</a>
</td>
<td align="left" width="63%">
Specifies the width of the rectangle.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidRect)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

