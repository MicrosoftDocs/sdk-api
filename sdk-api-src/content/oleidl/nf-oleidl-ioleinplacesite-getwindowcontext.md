---
UID: NF:oleidl.IOleInPlaceSite.GetWindowContext
title: IOleInPlaceSite::GetWindowContext (oleidl.h)
description: Enables an in-place object to retrieve the window interfaces that form the window object hierarchy, and the position in the parent window where the object's in-place activation window should be located.
helpviewer_keywords: ["GetWindowContext","GetWindowContext method [COM]","GetWindowContext method [COM]","IOleInPlaceSite interface","IOleInPlaceSite interface [COM]","GetWindowContext method","IOleInPlaceSite.GetWindowContext","IOleInPlaceSite::GetWindowContext","_ole_ioleinplacesite_getwindowcontext","com.ioleinplacesite_getwindowcontext","oleidl/IOleInPlaceSite::GetWindowContext"]
old-location: com\ioleinplacesite_getwindowcontext.htm
tech.root: com
ms.assetid: f6cf62b3-5a64-49aa-b0bd-56744ecee313
ms.date: 12/05/2018
ms.keywords: GetWindowContext, GetWindowContext method [COM], GetWindowContext method [COM],IOleInPlaceSite interface, IOleInPlaceSite interface [COM],GetWindowContext method, IOleInPlaceSite.GetWindowContext, IOleInPlaceSite::GetWindowContext, _ole_ioleinplacesite_getwindowcontext, com.ioleinplacesite_getwindowcontext, oleidl/IOleInPlaceSite::GetWindowContext
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IOleInPlaceSite::GetWindowContext
 - oleidl/IOleInPlaceSite::GetWindowContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleInPlaceSite.GetWindowContext
---

# IOleInPlaceSite::GetWindowContext


## -description

Enables an in-place object to retrieve the window interfaces that form the window object hierarchy, and the position in the parent window where the object's in-place activation window should be located.

## -parameters

### -param ppFrame [out]

A pointer to an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceframe">IOleInPlaceFrame</a> pointer variable that receives the interface pointer to the frame. If an error occurs, the implementation must set <i>ppFrame</i> to <b>NULL</b>.

### -param ppDoc [out]

A pointer to an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow">IOleInPlaceUIWindow</a> pointer variable that receives the interface pointer to the document window. If the document window is the same as the frame window, <i>ppDoc</i> is set to <b>NULL</b>. In this case, the object can only use <i>ppFrame</i> or border negotiation. If an error is returned, the implementation must set <i>ppDoc</i> to <b>NULL</b>.

### -param lprcPosRect [out]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure for the rectangle containing the position of the in-place object in the client coordinates of its parent window. If an error is returned, this parameter must be set to <b>NULL</b>.

### -param lprcClipRect [out]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure for the outer rectangle containing the in-place object's position rectangle (<i>lprcPosRect</i>). This rectangle is relative to the client area of the object's parent window. If an error is returned, this parameter must be set to <b>NULL</b>.

### -param lpFrameInfo [in, out]

A pointer to an <a href="/windows/win32/api/oleidl/ns-oleidl-oleinplaceframeinfo">OLEINPLACEFRAMEINFO</a> structure the container is to fill in with appropriate data. If an error is returned, this parameter must be set to <b>NULL</b>.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
 One or more of the supplied pointers is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/win32/api/oleidl/ns-oleidl-oleinplaceframeinfo">OLEINPLACEFRAMEINFO</a> structure provides data needed by OLE to dispatch keystroke accelerators to a container frame while an object is active in place.

When an object is activated, it calls <b>GetWindowContext</b> from its container. The container returns the handle to its in-place accelerator table through the <a href="/windows/win32/api/oleidl/ns-oleidl-oleinplaceframeinfo">OLEINPLACEFRAMEINFO</a> structure. Before calling <b>GetWindowContext</b>, the object must provide the size of the <b>OLEINPLACEFRAMEINFO</b> structure by filling in the cb member, pointed to by <i>lpFrameInfo</i>.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>