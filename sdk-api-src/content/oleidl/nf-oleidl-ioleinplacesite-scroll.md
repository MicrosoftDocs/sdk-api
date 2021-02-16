---
UID: NF:oleidl.IOleInPlaceSite.Scroll
title: IOleInPlaceSite::Scroll (oleidl.h)
description: Instructs the container to scroll the view of the object by the specified number of pixels.
helpviewer_keywords: ["IOleInPlaceSite interface [COM]","Scroll method","IOleInPlaceSite.Scroll","IOleInPlaceSite::Scroll","IOleInPlaceSiteWindowless.Scroll","Scroll","Scroll method [COM]","Scroll method [COM]","IOleInPlaceSite interface","_ole_ioleinplacesite_scroll","com.ioleinplacesite_scroll","oleidl/IOleInPlaceSite::Scroll"]
old-location: com\ioleinplacesite_scroll.htm
tech.root: com
ms.assetid: a169c4c6-b600-4812-bf71-d7fcd7486ff1
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSite interface [COM],Scroll method, IOleInPlaceSite.Scroll, IOleInPlaceSite::Scroll, IOleInPlaceSiteWindowless.Scroll, Scroll, Scroll method [COM], Scroll method [COM],IOleInPlaceSite interface, _ole_ioleinplacesite_scroll, com.ioleinplacesite_scroll, oleidl/IOleInPlaceSite::Scroll
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
 - IOleInPlaceSite::Scroll
 - oleidl/IOleInPlaceSite::Scroll
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
 - browsewm.dll
api_name:
 - IOleInPlaceSite.Scroll
 - IOleInPlaceSiteWindowless.Scroll
---

# IOleInPlaceSite::Scroll


## -description

Instructs the container to scroll the view of the object by the specified number of pixels.

## -parameters

### -param scrollExtant [in]

The number of pixels by which to scroll in the X and Y directions.

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
The specified pointer is not valid.

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

As a result of scrolling, the object's visible rectangle can change. If that happens, the container should give the new clipping rectangle to the object by calling <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-setobjectrects">IOleInPlaceObject::SetObjectRects</a>. The intersection of the <i>lprcClipRect</i> and <i>lprcPosRect</i> rectangles gives the new visible rectangle. See <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-getwindowcontext">IOleInPlaceSite::GetWindowContext</a> for more information.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Called by an active, in-place object when it is asking the container to scroll.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-setobjectrects">IOleInPlaceObject::SetObjectRects</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>