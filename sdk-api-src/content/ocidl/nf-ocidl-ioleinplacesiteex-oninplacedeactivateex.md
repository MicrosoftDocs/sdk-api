---
UID: NF:ocidl.IOleInPlaceSiteEx.OnInPlaceDeactivateEx
title: IOleInPlaceSiteEx::OnInPlaceDeactivateEx (ocidl.h)
description: Notifies the container if the object needs to be redrawn upon deactivation.
helpviewer_keywords: ["IOleInPlaceSiteEx interface [COM]","OnInPlaceDeactivateEx method","IOleInPlaceSiteEx.OnInPlaceDeactivateEx","IOleInPlaceSiteEx::OnInPlaceDeactivateEx","IOleInPlaceSiteWindowless.OnInPlaceDeactivateEx","OnInPlaceDeactivateEx","OnInPlaceDeactivateEx method [COM]","OnInPlaceDeactivateEx method [COM]","IOleInPlaceSiteEx interface","_ole_ioleinplacesiteex_oninplacedeactivateex","com.ioleinplacesiteex_oninplacedeactivateex","ocidl/IOleInPlaceSiteEx::OnInPlaceDeactivateEx"]
old-location: com\ioleinplacesiteex_oninplacedeactivateex.htm
tech.root: com
ms.assetid: c3c68b46-adca-4f8d-86c2-075b72f7c656
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSiteEx interface [COM],OnInPlaceDeactivateEx method, IOleInPlaceSiteEx.OnInPlaceDeactivateEx, IOleInPlaceSiteEx::OnInPlaceDeactivateEx, IOleInPlaceSiteWindowless.OnInPlaceDeactivateEx, OnInPlaceDeactivateEx, OnInPlaceDeactivateEx method [COM], OnInPlaceDeactivateEx method [COM],IOleInPlaceSiteEx interface, _ole_ioleinplacesiteex_oninplacedeactivateex, com.ioleinplacesiteex_oninplacedeactivateex, ocidl/IOleInPlaceSiteEx::OnInPlaceDeactivateEx
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
 - IOleInPlaceSiteEx::OnInPlaceDeactivateEx
 - ocidl/IOleInPlaceSiteEx::OnInPlaceDeactivateEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
 - wmp.dll
api_name:
 - IOleInPlaceSiteEx.OnInPlaceDeactivateEx
 - IOleInPlaceSiteWindowless.OnInPlaceDeactivateEx
---

# IOleInPlaceSiteEx::OnInPlaceDeactivateEx


## -description

Notifies the container if the object needs to be redrawn upon deactivation.

## -parameters

### -param fNoRedraw [in]

If <b>TRUE</b>, the container need not redraw the object after completing the deactivation; if <b>FALSE</b> the object must be redrawn after deactivation.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>

## -remarks

This method replaces <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-oninplacedeactivate">IOleInPlaceSite::OnInPlaceDeactivate</a>. If the older method is used, the object must always be redrawn on deactivation.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-oninplacedeactivate">IOleInPlaceSite::OnInPlaceDeactivate</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesiteex">IOleInPlaceSiteEx</a>