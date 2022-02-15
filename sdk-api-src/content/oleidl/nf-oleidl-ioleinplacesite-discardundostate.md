---
UID: NF:oleidl.IOleInPlaceSite.DiscardUndoState
title: IOleInPlaceSite::DiscardUndoState (oleidl.h)
description: Instructs the container to discard its undo state. The container should not call IOleInPlaceObject::ReActivateAndUndo.
helpviewer_keywords: ["DiscardUndoState","DiscardUndoState method [COM]","DiscardUndoState method [COM]","IOleInPlaceSite interface","IOleInPlaceSite interface [COM]","DiscardUndoState method","IOleInPlaceSite.DiscardUndoState","IOleInPlaceSite::DiscardUndoState","IOleInPlaceSiteWindowless.DiscardUndoState","_ole_ioleinplacesite_discardundostate","com.ioleinplacesite_discardundostate","oleidl/IOleInPlaceSite::DiscardUndoState"]
old-location: com\ioleinplacesite_discardundostate.htm
tech.root: com
ms.assetid: 8fe69aa5-a526-4e95-920b-01f84ae4ca83
ms.date: 12/05/2018
ms.keywords: DiscardUndoState, DiscardUndoState method [COM], DiscardUndoState method [COM],IOleInPlaceSite interface, IOleInPlaceSite interface [COM],DiscardUndoState method, IOleInPlaceSite.DiscardUndoState, IOleInPlaceSite::DiscardUndoState, IOleInPlaceSiteWindowless.DiscardUndoState, _ole_ioleinplacesite_discardundostate, com.ioleinplacesite_discardundostate, oleidl/IOleInPlaceSite::DiscardUndoState
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
 - IOleInPlaceSite::DiscardUndoState
 - oleidl/IOleInPlaceSite::DiscardUndoState
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
 - IOleInPlaceSite.DiscardUndoState
 - IOleInPlaceSiteWindowless.DiscardUndoState
---

# IOleInPlaceSite::DiscardUndoState


## -description

Instructs the container to discard its undo state. The container should not call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-reactivateandundo">IOleInPlaceObject::ReActivateAndUndo</a>.



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

If an object is activated in place and the object's associated object application maintains only one level of undo, there is no need to have more than one entry on the undo stack. That is, after a change has been made to the active object that invalidates its undo state saved by the container, there is no need to maintain this undo state in the container.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
<b>DiscardUndoState</b> is called by the active object while performing some action that would discard the undo state of the object. The in-place object calls this method to notify the container to discard the object's last saved undo state.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-discardundostate">IOleInPlaceSite::DiscardUndoState</a>
