---
UID: NF:oleidl.IOleInPlaceSite.DeactivateAndUndo
title: IOleInPlaceSite::DeactivateAndUndo
author: windows-sdk-content
description: Deactivates the object, ends the in-place session, and reverts to the container's saved undo state.
old-location: com\ioleinplacesite_deactivateandundo.htm
old-project: com
ms.assetid: 59229720-cd3b-45d5-90c4-391acb124f4d
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DeactivateAndUndo, DeactivateAndUndo method [COM], DeactivateAndUndo method [COM],IOleInPlaceSite interface, IOleInPlaceSite interface [COM],DeactivateAndUndo method, IOleInPlaceSite.DeactivateAndUndo, IOleInPlaceSite::DeactivateAndUndo, IOleInPlaceSiteWindowless.DeactivateAndUndo, _ole_ioleinplacesite_deactivateandundo, com.ioleinplacesite_deactivateandundo, oleidl/IOleInPlaceSite::DeactivateAndUndo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
 - browsewm.dll
api_name:
 - IOleInPlaceSite.DeactivateAndUndo
 - IOleInPlaceSiteWindowless.DeactivateAndUndo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleInPlaceSite::DeactivateAndUndo


## -description


Deactivates the object, ends the in-place session, and reverts to the container's saved undo state.


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



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Called by the active object when the user invokes undo just after activating the object.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Upon completion of this call, the container should call <a href="https://msdn.microsoft.com/cc42e313-b290-4806-bbad-b49abd937b63">IOleInPlaceObject::UIDeactivate</a> to remove the user interface for the object, activate itself, and undo.




## -see-also




<a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>
 

 

