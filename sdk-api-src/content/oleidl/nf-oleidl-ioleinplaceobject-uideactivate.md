---
UID: NF:oleidl.IOleInPlaceObject.UIDeactivate
title: IOleInPlaceObject::UIDeactivate (oleidl.h)
description: Deactivates and removes the user interface of an active in-place object.
helpviewer_keywords: ["IOleInPlaceObject interface [COM]","UIDeactivate method","IOleInPlaceObject.UIDeactivate","IOleInPlaceObject::UIDeactivate","UIDeactivate","UIDeactivate method [COM]","UIDeactivate method [COM]","IOleInPlaceObject interface","_ole_ioleinplaceobject_uideactivate","com.ioleinplaceobject_uideactivate","oleidl/IOleInPlaceObject::UIDeactivate"]
old-location: com\ioleinplaceobject_uideactivate.htm
tech.root: com
ms.assetid: cc42e313-b290-4806-bbad-b49abd937b63
ms.date: 12/05/2018
ms.keywords: IOleInPlaceObject interface [COM],UIDeactivate method, IOleInPlaceObject.UIDeactivate, IOleInPlaceObject::UIDeactivate, UIDeactivate, UIDeactivate method [COM], UIDeactivate method [COM],IOleInPlaceObject interface, _ole_ioleinplaceobject_uideactivate, com.ioleinplaceobject_uideactivate, oleidl/IOleInPlaceObject::UIDeactivate
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
 - IOleInPlaceObject::UIDeactivate
 - oleidl/IOleInPlaceObject::UIDeactivate
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
 - IOleInPlaceObject.UIDeactivate
---

# IOleInPlaceObject::UIDeactivate


## -description

Deactivates and removes the user interface of an active in-place object.



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
This method is called by the object's immediate container when, for example, the user has clicked in the client area outside the object.

If the container has called <b>IOleInPlaceObject::UIDeactivate</b>, it should later call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-inplacedeactivate">IOleInPlaceObject::InPlaceDeactivate</a> to properly clean up resources. The container can assume that stopping or releasing the object cleans up resources if necessary. The object must be prepared to do so if <b>IOleInPlaceObject::InPlaceDeactivate</b> has not been called. but either <b>IOleInPlaceObject::UIDeactivate</b> or <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a> has been called.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Resources such as menus and windows can be either cleaned up or kept in a hidden state until your object is completely deactivated by calls to either <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-inplacedeactivate">IOleInPlaceObject::InPlaceDeactivate</a> or <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>. The object application must call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-onuideactivate">IOleInPlaceSite::OnUIDeactivate</a> before doing anything with the composite menus so that the container can first be detached from the frame window. On deactivating the in-place object's user interface, the object is left in a ready state so it can be quickly reactivated. The object stays in this state until the undo state of the document changes. The container should then call <b>IOleInPlaceObject::InPlaceDeactivate</b> to tell the object to discard its undo state.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-inplacedeactivate">IOleInPlaceObject::InPlaceDeactivate</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-reactivateandundo">IOleInPlaceObject::ReactivateAndUndo</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-onuideactivate">IOleInPlaceSite::OnUIDeactivate</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>
