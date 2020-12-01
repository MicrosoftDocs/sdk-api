---
UID: NF:oleidl.IOleInPlaceObject.SetObjectRects
title: IOleInPlaceObject::SetObjectRects (oleidl.h)
description: Specifies how much of the in-place object is to be visible.
helpviewer_keywords: ["IOleInPlaceObject interface [COM]","SetObjectRects method","IOleInPlaceObject.SetObjectRects","IOleInPlaceObject::SetObjectRects","SetObjectRects","SetObjectRects method [COM]","SetObjectRects method [COM]","IOleInPlaceObject interface","_ole_ioleinplaceobject_setobjectrects","com.ioleinplaceobject_setobjectrects","oleidl/IOleInPlaceObject::SetObjectRects"]
old-location: com\ioleinplaceobject_setobjectrects.htm
tech.root: com
ms.assetid: 5ae2e44b-d2e2-4351-b4fa-8c37419a2bcb
ms.date: 12/05/2018
ms.keywords: IOleInPlaceObject interface [COM],SetObjectRects method, IOleInPlaceObject.SetObjectRects, IOleInPlaceObject::SetObjectRects, SetObjectRects, SetObjectRects method [COM], SetObjectRects method [COM],IOleInPlaceObject interface, _ole_ioleinplaceobject_setobjectrects, com.ioleinplaceobject_setobjectrects, oleidl/IOleInPlaceObject::SetObjectRects
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
 - IOleInPlaceObject::SetObjectRects
 - oleidl/IOleInPlaceObject::SetObjectRects
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
 - IOleInPlaceObject.SetObjectRects
---

# IOleInPlaceObject::SetObjectRects


## -description

Specifies how much of the in-place object is to be visible.

## -parameters

### -param lprcPosRect [in]

A pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the position of the in-place object using the client coordinates of its parent window.

### -param lprcClipRect [in]

A pointer to the outer rectangle containing the in-place object's position rectangle (<i>lprcPosRect</i>). This rectangle is relative to the client area of the object's parent window.

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
The specified pointer is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for the operation.

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

It is possible for <i>lprcClipRect</i> to change without <i>lprcPosRect</i> changing.

The size of an in-place object's rectangle is always calculated in pixels. This is different from other OLE object's visualizations, which are in <b>HIMETRIC</b>.

<div class="alert"><b>Note</b>  While executing <b>IOleInPlaceObject::SetObjectRects</b>, do not make calls to the <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> or <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a> functions, or a dialog box. Doing so may cause the system to deadlock. There are further restrictions on which OLE interface methods and functions can be called from within <b>IOleInPlaceObject::SetObjectRects</b>.</div>
<div> </div>
<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The container should call <b>IOleInPlaceObject::SetObjectRects</b> whenever the window position of the in-place object and/or the visible part of the in-place object changes.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The object must size its in-place window to match the intersection of <i>lprcPosRect</i> and <i>lprcClipRect</i>. The object must also draw its contents into the object's in-place window so that proper clipping takes place.

The object should compare its width and height with those provided by its container (conveyed through <i>lprcPosRect</i>). If the comparison does not result in a match, the container is applying scaling to the object. The object must then decide whether it should continue the in-place editing in the scale/zoom mode or deactivate.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-onposrectchange">IOleInPlaceSite::OnPosRectChange</a>



<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>