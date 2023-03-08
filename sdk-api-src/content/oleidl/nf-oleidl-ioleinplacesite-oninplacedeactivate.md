---
UID: NF:oleidl.IOleInPlaceSite.OnInPlaceDeactivate
title: IOleInPlaceSite::OnInPlaceDeactivate (oleidl.h)
description: Notifies the container that the object is no longer active in place.
helpviewer_keywords: ["IOleInPlaceSite interface [COM]","OnInPlaceDeactivate method","IOleInPlaceSite.OnInPlaceDeactivate","IOleInPlaceSite::OnInPlaceDeactivate","OnInPlaceDeactivate","OnInPlaceDeactivate method [COM]","OnInPlaceDeactivate method [COM]","IOleInPlaceSite interface","_ole_ioleinplacesite_oninplacedeactivate","com.ioleinplacesite_oninplacedeactivate","oleidl/IOleInPlaceSite::OnInPlaceDeactivate"]
old-location: com\ioleinplacesite_oninplacedeactivate.htm
tech.root: com
ms.assetid: 070aac4e-94b6-4e23-b132-1dc833774c8b
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSite interface [COM],OnInPlaceDeactivate method, IOleInPlaceSite.OnInPlaceDeactivate, IOleInPlaceSite::OnInPlaceDeactivate, OnInPlaceDeactivate, OnInPlaceDeactivate method [COM], OnInPlaceDeactivate method [COM],IOleInPlaceSite interface, _ole_ioleinplacesite_oninplacedeactivate, com.ioleinplacesite_oninplacedeactivate, oleidl/IOleInPlaceSite::OnInPlaceDeactivate
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
 - IOleInPlaceSite::OnInPlaceDeactivate
 - oleidl/IOleInPlaceSite::OnInPlaceDeactivate
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
 - IOleInPlaceSite.OnInPlaceDeactivate
---

# IOleInPlaceSite::OnInPlaceDeactivate


## -description

Notifies the container that the object is no longer active in place.



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

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
<b>OnInPlaceDeactivate</b> is called by an in-place object when it is fully deactivated. This function notifies the container that the object has been deactivated, and it gives the container a chance to run code pertinent to the object's deactivation. In particular, <b>OnInPlaceDeactivate</b> is called as a result of <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-inplacedeactivate">IOleInPlaceObject::InPlaceDeactivate</a> being called. Calling <b>OnInPlaceDeactivate</b> indicates that the object can no longer support Undo.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the container is holding pointers to the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a> and <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceactiveobject">IOleInPlaceActiveObject</a> interface implementations, it should release them after the <b>OnInPlaceDeactivate</b> call.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-inplacedeactivate">IOleInPlaceObject::InPlaceDeactivate</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>
