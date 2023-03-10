---
UID: NF:oleidl.IOleInPlaceObject.InPlaceDeactivate
title: IOleInPlaceObject::InPlaceDeactivate (oleidl.h)
description: Deactivates an active in-place object and discards the object's undo state.
helpviewer_keywords: ["IOleInPlaceObject interface [COM]","InPlaceDeactivate method","IOleInPlaceObject.InPlaceDeactivate","IOleInPlaceObject::InPlaceDeactivate","InPlaceDeactivate","InPlaceDeactivate method [COM]","InPlaceDeactivate method [COM]","IOleInPlaceObject interface","_ole_ioleinplaceobject_inplacedeactivate","com.ioleinplaceobject_inplacedeactivate","oleidl/IOleInPlaceObject::InPlaceDeactivate"]
old-location: com\ioleinplaceobject_inplacedeactivate.htm
tech.root: com
ms.assetid: 174a8bde-0795-4d4d-a294-7708c7d1823a
ms.date: 12/05/2018
ms.keywords: IOleInPlaceObject interface [COM],InPlaceDeactivate method, IOleInPlaceObject.InPlaceDeactivate, IOleInPlaceObject::InPlaceDeactivate, InPlaceDeactivate, InPlaceDeactivate method [COM], InPlaceDeactivate method [COM],IOleInPlaceObject interface, _ole_ioleinplaceobject_inplacedeactivate, com.ioleinplaceobject_inplacedeactivate, oleidl/IOleInPlaceObject::InPlaceDeactivate
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
 - IOleInPlaceObject::InPlaceDeactivate
 - oleidl/IOleInPlaceObject::InPlaceDeactivate
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
 - IOleInPlaceObject.InPlaceDeactivate
---

# IOleInPlaceObject::InPlaceDeactivate


## -description

Deactivates an active in-place object and discards the object's undo state.



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
An unexpected error occurred.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
This method is called by an active object's immediate container to deactivate the active object and discard its undo state.


<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
On return from <b>IOleInPlaceObject::InPlaceDeactivate</b>, the object discards its undo state. The object application should not shut down immediately after this call. Instead, it should wait for an explicit call to <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a> or for the object's reference count to reach zero.

Before deactivating, the object application should give the container a chance to put its user interface back on the frame window by calling <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-onuideactivate">IOleInPlaceSite::OnUIDeactivate</a>.

If the in-place user interface is still visible during the call to <b>IOleInPlaceObject::InPlaceDeactivate</b>, the object application should call its own <b>IOleInPlaceObject::InPlaceDeactivate</b> method to hide the user interface. The in-place user interface can be optionally destroyed during calls to <b>IOleInPlaceObject::InPlaceDeactivate</b> and <b>IOleInPlaceObject::InPlaceDeactivate</b>. But if the user interface has not already been destroyed when the container calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>, then it must be destroyed during the call to <b>IOleObject::Close</b>.

During the call to <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>, the object should check to see whether it is still active in place. If so, it should call <b>IOleInPlaceObject::InPlaceDeactivate</b>.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-oninplacedeactivate">IOleInPlaceSite::OnInPlaceDeactivate</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-onuideactivate">IOleInPlaceSite::OnUIDeactivate</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>
