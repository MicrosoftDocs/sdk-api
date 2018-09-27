---
UID: NF:oleidl.IOleInPlaceSite.DiscardUndoState
title: IOleInPlaceSite::DiscardUndoState
author: windows-sdk-content
description: Instructs the container to discard its undo state. The container should not call IOleInPlaceObject::ReActivateAndUndo.
old-location: com\ioleinplacesite_discardundostate.htm
tech.root: com
ms.assetid: 8fe69aa5-a526-4e95-920b-01f84ae4ca83
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DiscardUndoState, DiscardUndoState method [COM], DiscardUndoState method [COM],IOleInPlaceSite interface, IOleInPlaceSite interface [COM],DiscardUndoState method, IOleInPlaceSite.DiscardUndoState, IOleInPlaceSite::DiscardUndoState, IOleInPlaceSiteWindowless.DiscardUndoState, _ole_ioleinplacesite_discardundostate, com.ioleinplacesite_discardundostate, oleidl/IOleInPlaceSite::DiscardUndoState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleInPlaceSite::DiscardUndoState


## -description


Instructs the container to discard its undo state. The container should not call <a href="https://msdn.microsoft.com/b41bbfd6-1a86-4ca6-9d4b-c87c4feea7c3">IOleInPlaceObject::ReActivateAndUndo</a>.


## -parameters






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




<a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>



<a href="https://msdn.microsoft.com/8fe69aa5-a526-4e95-920b-01f84ae4ca83">IOleInPlaceSite::DiscardUndoState</a>
 

 

