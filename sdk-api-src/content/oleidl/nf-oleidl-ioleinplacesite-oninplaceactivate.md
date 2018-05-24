---
UID: NF:oleidl.IOleInPlaceSite.OnInPlaceActivate
title: IOleInPlaceSite::OnInPlaceActivate
author: windows-driver-content
description: Notifies the container that one of its objects is being activated in place.
old-location: com\ioleinplacesite_oninplaceactivate.htm
old-project: com
ms.assetid: e5744911-1ea6-4482-988d-8def16229f4c
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IOleInPlaceSite interface [COM],OnInPlaceActivate method, IOleInPlaceSite.OnInPlaceActivate, IOleInPlaceSite::OnInPlaceActivate, OnInPlaceActivate, OnInPlaceActivate method [COM], OnInPlaceActivate method [COM],IOleInPlaceSite interface, _ole_ioleinplacesite_oninplaceactivate, com.ioleinplacesite_oninplaceactivate, oleidl/IOleInPlaceSite::OnInPlaceActivate
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
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleInPlaceSite.OnInPlaceActivate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleInPlaceSite::OnInPlaceActivate


## -description


Notifies the container that one of its objects is being activated in place.


## -parameters






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
<b>OnInPlaceActivate</b> is called by the active embedded object when it is activated in-place for the first time. The container should note that the object is becoming active.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
A container that supports linking to embedded objects must properly manage the running of its in-place objects when they are UI-inactive and running in the hidden state. To reactivate the in-place object quickly, a container should not call <a href="https://msdn.microsoft.com/61ecd153-ed6b-4a2c-a862-54742c5769ee">IOleObject::Close</a> until the container's <a href="https://msdn.microsoft.com/59229720-cd3b-45d5-90c4-391acb124f4d">IOleInPlaceSite::DeactivateAndUndo</a> method is called. To help protect against the object being left in an unstable state if a linking client updates silently, the container should call <a href="https://msdn.microsoft.com/84941a59-6880-4824-b4b9-cd1b52d2bffb">OleLockRunning</a> to lock the object in the running state. This prevents the hidden in-place object from shutting down before it can be saved in its container.




## -see-also




<a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>
 

 

