---
UID: NN:ocidl.IOleInPlaceSiteWindowless
title: IOleInPlaceSiteWindowless (ocidl.h)
description: Extends the IOleInPlaceSiteEx interface.
old-location: com\ioleinplacesitewindowless.htm
tech.root: com
ms.assetid: 4ad83599-99d2-4b35-95de-cff845a8d5e4
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSiteWindowless, IOleInPlaceSiteWindowless interface [COM], IOleInPlaceSiteWindowless interface [COM],described, _ole_ioleinplacesitewindowless, com.ioleinplacesitewindowless, ocidl/IOleInPlaceSiteWindowless
f1_keywords:
- ocidl/IOleInPlaceSiteWindowless
dev_langs:
- c++
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
- OCIdl.h
api_name:
- IOleInPlaceSiteWindowless
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleInPlaceSiteWindowless interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesiteex">IOleInPlaceSiteEx</a> interface. <b>IOleInPlaceSiteWindowless</b> works with <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless">IOleInPlaceObjectWindowless</a> which is implemented on the windowless object. Together, these two interfaces provide services to a windowless object from its container allowing the windowless object to:
<ul>
<li>Process window messages</li>
<li>Participate in drag and drop operations
</li>
<li>Perform drawing operations</li>
</ul>Having a window can place unnecessary burdens on small objects, such as controls. It prevents an object from being non-rectangular. It prevents windows from being transparent. It prevents the small instance size needed by many small controls.

A windowless object can enter the in-place active state without requiring a window or the resources associated with a window. Instead, the object's container provides the object with many of the services associated with having a window.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleInPlaceSiteWindowless</b> interface inherits from <b>IOleInPlaceSiteEx</b>. <b>IOleInPlaceSiteWindowless</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleInPlaceSiteWindowless</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-adjustrect">AdjustRect</a>
</td>
<td align="left" width="63%">
Adjusts a specified rectangle if it is entirely or partially covered by overlapping, opaque objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-canwindowlessactivate">CanWindowlessActivate</a>
</td>
<td align="left" width="63%">
Informs an object if its container can support it as a windowless object that can be in-place activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-getcapture">GetCapture</a>
</td>
<td align="left" width="63%">
Called by an in-place active, windowless object to determine whether it still has the mouse capture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-getdc">GetDC</a>
</td>
<td align="left" width="63%">
Provides an object with a handle to a device context for a screen or compatible device from its container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-getfocus">GetFocus</a>
</td>
<td align="left" width="63%">
Called by an in-place active, windowless object to determine whether it still has the keyboard focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-invalidaterect">InvalidateRect</a>
</td>
<td align="left" width="63%">
Enables an object to invalidate a specified rectangle of its in-place image on the screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-invalidatergn">InvalidateRgn</a>
</td>
<td align="left" width="63%">
Enables an object to invalidate a specified region of its in-place image on the screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-ondefwindowmessage">OnDefWindowMessage</a>
</td>
<td align="left" width="63%">
Invokes the default processing for all messages passed to an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-releasedc">ReleaseDC</a>
</td>
<td align="left" width="63%">
Releases the device context previously obtained by a call to <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-getdc">IOleInPlaceSiteWindowless::GetDC</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-scrollrect">ScrollRect</a>
</td>
<td align="left" width="63%">
Enables an object to scroll an area within its in-place active image on the screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-setcapture">SetCapture</a>
</td>
<td align="left" width="63%">
Enables an in-place active, windowless object to capture all mouse messages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-setfocus">SetFocus</a>
</td>
<td align="left" width="63%">
Sets the keyboard focus for a UI-active, windowless object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iadvisesinkex">IAdviseSinkEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iolecontrol">IOleControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceactiveobject-translateaccelerator">IOleInPlaceActiveObject::TranslateAccelerator</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless">IOleInPlaceObjectWindowless</a>
 

 

