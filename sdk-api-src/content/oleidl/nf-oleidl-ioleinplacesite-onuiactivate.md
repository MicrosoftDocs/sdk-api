---
UID: NF:oleidl.IOleInPlaceSite.OnUIActivate
title: IOleInPlaceSite::OnUIActivate (oleidl.h)
description: Notifies the container that the object is about to be activated in place and that the object is going to replace the container's main menu with an in-place composite menu.
helpviewer_keywords: ["IOleInPlaceSite interface [COM]","OnUIActivate method","IOleInPlaceSite.OnUIActivate","IOleInPlaceSite::OnUIActivate","OnUIActivate","OnUIActivate method [COM]","OnUIActivate method [COM]","IOleInPlaceSite interface","_ole_ioleinplacesite_onuiactivate","com.ioleinplacesite_onuiactivate","oleidl/IOleInPlaceSite::OnUIActivate"]
old-location: com\ioleinplacesite_onuiactivate.htm
tech.root: com
ms.assetid: d863805c-58c1-4e35-84b5-72f01a4ba205
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSite interface [COM],OnUIActivate method, IOleInPlaceSite.OnUIActivate, IOleInPlaceSite::OnUIActivate, OnUIActivate, OnUIActivate method [COM], OnUIActivate method [COM],IOleInPlaceSite interface, _ole_ioleinplacesite_onuiactivate, com.ioleinplacesite_onuiactivate, oleidl/IOleInPlaceSite::OnUIActivate
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
 - IOleInPlaceSite::OnUIActivate
 - oleidl/IOleInPlaceSite::OnUIActivate
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
 - IOleInPlaceSite.OnUIActivate
---

# IOleInPlaceSite::OnUIActivate


## -description

Notifies the container that the object is about to be activated in place and that the object is going to replace the container's main menu with an in-place composite menu.



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

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The in-place object calls <b>IOleInPlaceSite::OnUIActivate</b> just before activating its user interface.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The container should remove any user interface associated with its own activation. If the container is itself an embedded object, it should remove its document-level user interface.

If there is already an object active in place in the same document, the container should call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-uideactivate">IOleInPlaceObject::UIDeactivate</a> before calling <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-onuideactivate">OnUIDeactivate</a>.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-uideactivate">IOleInPlaceObject::UIDeactivate</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>
