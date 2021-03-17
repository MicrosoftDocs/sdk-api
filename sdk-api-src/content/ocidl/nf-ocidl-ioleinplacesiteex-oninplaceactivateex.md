---
UID: NF:ocidl.IOleInPlaceSiteEx.OnInPlaceActivateEx
title: IOleInPlaceSiteEx::OnInPlaceActivateEx (ocidl.h)
description: Called by the embedded object to determine whether it needs to redraw itself upon activation.
helpviewer_keywords: ["IOleInPlaceSiteEx interface [COM]","OnInPlaceActivateEx method","IOleInPlaceSiteEx.OnInPlaceActivateEx","IOleInPlaceSiteEx::OnInPlaceActivateEx","OnInPlaceActivateEx","OnInPlaceActivateEx method [COM]","OnInPlaceActivateEx method [COM]","IOleInPlaceSiteEx interface","_ole_ioleinplacesiteex_oninplaceactivateex","com.ioleinplacesiteex_oninplaceactivateex","ocidl/IOleInPlaceSiteEx::OnInPlaceActivateEx"]
old-location: com\ioleinplacesiteex_oninplaceactivateex.htm
tech.root: com
ms.assetid: 11c96c79-9884-4bac-828b-53ac4de65182
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSiteEx interface [COM],OnInPlaceActivateEx method, IOleInPlaceSiteEx.OnInPlaceActivateEx, IOleInPlaceSiteEx::OnInPlaceActivateEx, OnInPlaceActivateEx, OnInPlaceActivateEx method [COM], OnInPlaceActivateEx method [COM],IOleInPlaceSiteEx interface, _ole_ioleinplacesiteex_oninplaceactivateex, com.ioleinplacesiteex_oninplaceactivateex, ocidl/IOleInPlaceSiteEx::OnInPlaceActivateEx
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
 - IOleInPlaceSiteEx::OnInPlaceActivateEx
 - ocidl/IOleInPlaceSiteEx::OnInPlaceActivateEx
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
 - IOleInPlaceSiteEx.OnInPlaceActivateEx
---

# IOleInPlaceSiteEx::OnInPlaceActivateEx


## -description

Called by the embedded object to determine whether it needs to redraw itself upon activation.

## -parameters

### -param pfNoRedraw [out]

A pointer to a variable that receives the current redraw status. The status is <b>TRUE</b> if the object need not redraw itself upon activation and <b>FALSE</b> otherwise. Windowless objects usually do not need the value returned by this parameter and may pass a <b>NULL</b> pointer to save the container the burden of computing this value.

### -param dwFlags [in]

Indicates whether the object is activated as a windowless object. This parameter takes values from the <a href="/windows/desktop/api/ocidl/ne-ocidl-activateflags">ACTIVATEFLAGS</a> enumeration. See <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a> for more information on windowless objects.

## -returns

This method returns S_OK if the container allows the in-place activation.
Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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

This method replaces <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-oninplaceactivate">IOleInPlaceSite::OnInPlaceActivate</a>. If the older method is used, the object must always redraw itself on activation.

Windowless objects are required to use this method instead of <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-oninplaceactivate">IOleInPlaceSite::OnInPlaceActivate</a> to notify the container of whether they are activating windowless or not.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The container should carefully check the invalidation status of the object, its z-order, clipping and any other relevant parameters to determine the appropriate value to return in <i>pfNoRedraw</i>.

A container can cache the value of the <a href="/windows/desktop/api/ocidl/ne-ocidl-activateflags">ACTIVATEFLAGS</a> enumeration instead of calling the <a href="/windows/desktop/api/oleidl/nf-oleidl-iolewindow-getwindow">GetWindow</a> method in the <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless">IOleInPlaceObjectWindowless</a> interface repeatedly.

## -see-also

<a href="/windows/desktop/api/ocidl/ne-ocidl-activateflags">ACTIVATEFLAGS</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless">IOleInPlaceObjectWindowless</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-oninplaceactivate">IOleInPlaceSite::OnInPlaceActivate</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesiteex">IOleInPlaceSiteEx</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>