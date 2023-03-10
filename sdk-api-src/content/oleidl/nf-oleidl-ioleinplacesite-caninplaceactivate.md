---
UID: NF:oleidl.IOleInPlaceSite.CanInPlaceActivate
title: IOleInPlaceSite::CanInPlaceActivate (oleidl.h)
description: Determines whether the container can activate the object in place.
helpviewer_keywords: ["CanInPlaceActivate","CanInPlaceActivate method [COM]","CanInPlaceActivate method [COM]","IOleInPlaceSite interface","IOleInPlaceSite interface [COM]","CanInPlaceActivate method","IOleInPlaceSite.CanInPlaceActivate","IOleInPlaceSite::CanInPlaceActivate","_ole_ioleinplacesite_caninplaceactivate","com.ioleinplacesite_caninplaceactivate","oleidl/IOleInPlaceSite::CanInPlaceActivate"]
old-location: com\ioleinplacesite_caninplaceactivate.htm
tech.root: com
ms.assetid: ac960359-7e02-43b6-ac42-0000af15b1a4
ms.date: 12/05/2018
ms.keywords: CanInPlaceActivate, CanInPlaceActivate method [COM], CanInPlaceActivate method [COM],IOleInPlaceSite interface, IOleInPlaceSite interface [COM],CanInPlaceActivate method, IOleInPlaceSite.CanInPlaceActivate, IOleInPlaceSite::CanInPlaceActivate, _ole_ioleinplacesite_caninplaceactivate, com.ioleinplacesite_caninplaceactivate, oleidl/IOleInPlaceSite::CanInPlaceActivate
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
 - IOleInPlaceSite::CanInPlaceActivate
 - oleidl/IOleInPlaceSite::CanInPlaceActivate
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
 - IOleInPlaceSite.CanInPlaceActivate
---

# IOleInPlaceSite::CanInPlaceActivate


## -description

Determines whether the container can activate the object in place.



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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The container does not allow in-place activation for this object.

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

Only objects being displayed as DVASPECT_CONTENT can be activated in place.


<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
<b>CanInPlaceActivate</b> is called by the client site's immediate child object when this object must activate in place. This function allows the container application to accept or refuse the activation request.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>
