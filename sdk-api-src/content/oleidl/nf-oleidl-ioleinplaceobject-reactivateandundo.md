---
UID: NF:oleidl.IOleInPlaceObject.ReactivateAndUndo
title: IOleInPlaceObject::ReactivateAndUndo (oleidl.h)
description: Reactivates a previously deactivated object, undoing the last state of the object.
helpviewer_keywords: ["IOleInPlaceObject interface [COM]","ReactivateAndUndo method","IOleInPlaceObject.ReactivateAndUndo","IOleInPlaceObject::ReactivateAndUndo","ReactivateAndUndo","ReactivateAndUndo method [COM]","ReactivateAndUndo method [COM]","IOleInPlaceObject interface","_ole_ioleinplaceobject_reactivateandundo","com.ioleinplaceobject_reactivateandundo","oleidl/IOleInPlaceObject::ReactivateAndUndo"]
old-location: com\ioleinplaceobject_reactivateandundo.htm
tech.root: com
ms.assetid: b41bbfd6-1a86-4ca6-9d4b-c87c4feea7c3
ms.date: 12/05/2018
ms.keywords: IOleInPlaceObject interface [COM],ReactivateAndUndo method, IOleInPlaceObject.ReactivateAndUndo, IOleInPlaceObject::ReactivateAndUndo, ReactivateAndUndo, ReactivateAndUndo method [COM], ReactivateAndUndo method [COM],IOleInPlaceObject interface, _ole_ioleinplaceobject_reactivateandundo, com.ioleinplaceobject_reactivateandundo, oleidl/IOleInPlaceObject::ReactivateAndUndo
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
 - IOleInPlaceObject::ReactivateAndUndo
 - oleidl/IOleInPlaceObject::ReactivateAndUndo
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
 - IOleInPlaceObject.ReactivateAndUndo
---

# IOleInPlaceObject::ReactivateAndUndo


## -description

Reactivates a previously deactivated object, undoing the last state of the object.



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
<dt><b>E_NOTUNDOABLE</b></dt>
</dl>
</td>
<td width="60%">
The undo state is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for the operation.

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

If the user chooses the <b>Undo</b> command before the undo state of the object is lost, the object's immediate container calls <b>IOleInPlaceObject::ReactivateAndUndo</b> to activate the user interface, carry out the undo operation, and return the object to the active state.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a>
