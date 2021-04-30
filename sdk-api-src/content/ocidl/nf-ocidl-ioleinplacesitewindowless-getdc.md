---
UID: NF:ocidl.IOleInPlaceSiteWindowless.GetDC
title: IOleInPlaceSiteWindowless::GetDC (ocidl.h)
description: Provides an object with a handle to a device context for a screen or compatible device from its container.
helpviewer_keywords: ["GetDC","GetDC method [COM]","GetDC method [COM]","IOleInPlaceSiteWindowless interface","IOleInPlaceSiteWindowless interface [COM]","GetDC method","IOleInPlaceSiteWindowless.GetDC","IOleInPlaceSiteWindowless::GetDC","_ole_ioleinplacesitewindowless_getdc","com.ioleinplacesitewindowless_getdc","ocidl/IOleInPlaceSiteWindowless::GetDC"]
old-location: com\ioleinplacesitewindowless_getdc.htm
tech.root: com
ms.assetid: 232587a8-ed88-4339-9e28-6e34be263a51
ms.date: 12/05/2018
ms.keywords: GetDC, GetDC method [COM], GetDC method [COM],IOleInPlaceSiteWindowless interface, IOleInPlaceSiteWindowless interface [COM],GetDC method, IOleInPlaceSiteWindowless.GetDC, IOleInPlaceSiteWindowless::GetDC, _ole_ioleinplacesitewindowless_getdc, com.ioleinplacesitewindowless_getdc, ocidl/IOleInPlaceSiteWindowless::GetDC
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleInPlaceSiteWindowless::GetDC
 - ocidl/IOleInPlaceSiteWindowless::GetDC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleInPlaceSiteWindowless.GetDC
---

# IOleInPlaceSiteWindowless::GetDC


## -description

Provides an object with a handle to a device context for a screen or compatible device from its container.

## -parameters

### -param pRect [in]

A pointer to the rectangle that the object wants to redraw, in client coordinates of the containing window. If this parameter is <b>NULL</b>, the object's full extent is redrawn.

### -param grfFlags [in]

A combination of values from the <a href="/windows/desktop/api/ocidl/ne-ocidl-oledcflags">OLEDCFLAGS</a> enumeration.

### -param phDC [out]

A pointer to a returned device context.

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
<dt><b>OLE_E_NESTEDPAINT</b></dt>
</dl>
</td>
<td width="60%">
The container is already in the middle of a paint session. That is, this method has already been called, and the <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-releasedc">IOleInPlaceSiteWindowless::ReleaseDC</a> method has not yet been called.

</td>
</tr>
</table>

## -remarks

A device context obtained by this method should be released by calling <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-releasedc">IOleInPlaceSiteWindowless::ReleaseDC</a>.

Like other methods in this interface, rectangles are specified in client coordinates of the containing window. The container is expected to intersect this rectangle with the object's site rectangle and clip out everything outside the resulting rectangle. This prevents objects from inadvertently drawing where they are not supposed to.

Containers are also expected to map the device context origin so the object can draw in client coordinates of the containing window, usually the container's window. If the container is merely passing its window device context, this occurs automatically. If it is returning another device context, for example, an offscreen memory device context, then the viewport origin should be set appropriately.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Depending whether it is returning an on-screen or off-screen device context and depending on how sophisticated it is, container can use one of the following algorithms:

<ol>
<li>
On-screen, One Pass Drawing

<ol>
<li>In the <b>IOleInPlaceSiteWindowless::GetDC</b> method, the container should:<ul>
<li>Get the window device context.</li>
<li>If <a href="/windows/desktop/api/ocidl/ne-ocidl-oledcflags">OLEDC</a>_PAINTBKGND is set, draw the <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>_CONTENT aspect of every object behind the object requesting the device context.</li>
<li>Return the device context.</li>
</ul>
</li>
<li>In the <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-releasedc">ReleaseDC</a> method, the container should:<ul>
<li>Draw the DVASPECT_CONTENT of every overlapping object.</li>
<li>Release the device context.</li>
</ul>
</li>
</ol>
</li>
<li>
On-screen, Two Pass Drawing

<ol>
<li>In the <b>IOleInPlaceSiteWindowless::GetDC</b> method, the container should:<ul>
<li>Get the window device context.</li>
<li>Clip out the opaque regions of any overlapping object. These regions do not need to be redrawn since they are already correct on the screen.
</li>
<li>If OLEDC_PAINTBKGND is not set, return the device context.</li>
<li>Otherwise, clip out the opaque parts of the object requesting the device context and draw the opaque parts of every object behind it going front to back.</li>
<li>Draw the transparent aspects of every object behind going back to front, setting the clipping region appropriately each time.</li>
<li>Finally return the device context.</li>
</ul>
</li>
<li>In the <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-releasedc">IOleInPlaceSiteWindowless::ReleaseDC</a> method, the container should:<ul>
<li>Draw the transparent parts of every overlapping object.</li>
<li>Release the device context.</li>
</ul>
</li>
</ol>
</li>
<li>
 Off-screen Drawing

<ol>
<li>In the <b>IOleInPlaceSiteWindowless::GetDC</b> method, the container should:<ul>
<li>Create a screen compatible memory device context, containing a compatible bitmap of appropriate size.</li>
<li>Map the viewport origin of the device context to ensure that the calling object can draw using client area coordinates of the containing window.</li>
<li>If OLEDC_PAINTBKGND is set, draw the DVASPECT_CONTENT of every object behind the calling object.</li>
<li>Return the device context.</li>
</ul>
</li>
<li>In the <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-releasedc">IOleInPlaceSiteWindowless::ReleaseDC</a> method, the container should:<ul>
<li>Draw the DVASPECT_CONTENT aspect of every overlapping object.</li>
<li>Copy the off-screen bitmap to the screen at the location the calling object originally requested in <b>IOleInPlaceSiteWindowless::GetDC</b>.</li>
<li>Delete and release the memory device context.</li>
</ul>
</li>
</ol>
</li>
</ol>
When this method returns, the clipping region in the device context should be set so that the object can't paint in any area it is not supposed to. If the object is not opaque, the background should have been painted. If the device context is a screen, any overlapping opaque areas should be clipped out.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-releasedc">IOleInPlaceSiteWindowless::ReleaseDC</a>



<a href="/windows/desktop/api/ocidl/ne-ocidl-oledcflags">OLEDCFLAGS</a>