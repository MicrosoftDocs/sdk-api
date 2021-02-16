---
UID: NF:oleidl.IOleInPlaceSite.OnUIDeactivate
title: IOleInPlaceSite::OnUIDeactivate (oleidl.h)
description: Notifies the container that it should reinstall its user interface and take focus, and whether the object has an undoable state.
helpviewer_keywords: ["IOleInPlaceSite interface [COM]","OnUIDeactivate method","IOleInPlaceSite.OnUIDeactivate","IOleInPlaceSite::OnUIDeactivate","IOleInPlaceSiteWindowless.OnUIDeactivate","OnUIDeactivate","OnUIDeactivate method [COM]","OnUIDeactivate method [COM]","IOleInPlaceSite interface","_ole_ioleinplacesite_onuideactivate","com.ioleinplacesite_onuideactivate","oleidl/IOleInPlaceSite::OnUIDeactivate"]
old-location: com\ioleinplacesite_onuideactivate.htm
tech.root: com
ms.assetid: 926c02b4-0bfa-4509-b5bc-4e5007e4db1a
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSite interface [COM],OnUIDeactivate method, IOleInPlaceSite.OnUIDeactivate, IOleInPlaceSite::OnUIDeactivate, IOleInPlaceSiteWindowless.OnUIDeactivate, OnUIDeactivate, OnUIDeactivate method [COM], OnUIDeactivate method [COM],IOleInPlaceSite interface, _ole_ioleinplacesite_onuideactivate, com.ioleinplacesite_onuideactivate, oleidl/IOleInPlaceSite::OnUIDeactivate
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
 - IOleInPlaceSite::OnUIDeactivate
 - oleidl/IOleInPlaceSite::OnUIDeactivate
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
 - IOleInPlaceSite.OnUIDeactivate
 - IOleInPlaceSiteWindowless.OnUIDeactivate
---

# IOleInPlaceSite::OnUIDeactivate


## -description

Notifies the container that it should reinstall its user interface and take focus, and whether the object has an undoable state.

## -parameters

### -param fUndoable [in]

Specifies whether the object can undo changes (TRUE) or not (FALSE).

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

The object indicates whether it can undo changes through the <i>fUndoable</i> flag. If the object can undo changes, the container can (by the user invoking the <b>Edit Undo</b> command) call the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-reactivateandundo">IOleInPlaceObject::ReactivateAndUndo</a> method to undo the changes.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
<b>IOleInPlaceSite::OnUIDeactivate</b> is called by the site's immediate child object when it is deactivating to notify the container that it should reinstall its own user interface components and take focus. The container should wait for the call to <b>IOleInPlaceSite::OnUIDeactivate</b> to complete before fully cleaning up and destroying any composite submenus.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-reactivateandundo">IOleInPlaceObject::ReactivateAndUndo</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>