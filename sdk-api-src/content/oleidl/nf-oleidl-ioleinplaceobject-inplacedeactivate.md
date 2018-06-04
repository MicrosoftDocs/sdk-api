---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IOleInPlaceObject::InPlaceDeactivate


## -description


Deactivates an active in-place object and discards the object's undo state.


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
An unexpected error occurred.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
This method is called by an active object's immediate container to deactivate the active object and discard its undo state.


<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
On return from <b>IOleInPlaceObject::InPlaceDeactivate</b>, the object discards its undo state. The object application should not shut down immediately after this call. Instead, it should wait for an explicit call to <a href="https://msdn.microsoft.com/61ecd153-ed6b-4a2c-a862-54742c5769ee">IOleObject::Close</a> or for the object's reference count to reach zero.

Before deactivating, the object application should give the container a chance to put its user interface back on the frame window by calling <a href="https://msdn.microsoft.com/926c02b4-0bfa-4509-b5bc-4e5007e4db1a">IOleInPlaceSite::OnUIDeactivate</a>.

If the in-place user interface is still visible during the call to <b>IOleInPlaceObject::InPlaceDeactivate</b>, the object application should call its own <b>IOleInPlaceObject::InPlaceDeactivate</b> method to hide the user interface. The in-place user interface can be optionally destroyed during calls to <b>IOleInPlaceObject::InPlaceDeactivate</b> and <b>IOleInPlaceObject::InPlaceDeactivate</b>. But if the user interface has not already been destroyed when the container calls <a href="https://msdn.microsoft.com/61ecd153-ed6b-4a2c-a862-54742c5769ee">IOleObject::Close</a>, then it must be destroyed during the call to <b>IOleObject::Close</b>.

During the call to <a href="https://msdn.microsoft.com/61ecd153-ed6b-4a2c-a862-54742c5769ee">IOleObject::Close</a>, the object should check to see whether it is still active in place. If so, it should call <b>IOleInPlaceObject::InPlaceDeactivate</b>.




## -see-also




<a href="https://msdn.microsoft.com/c14de79d-e844-49cf-ae70-6c3e417fab90">IOleInPlaceObject</a>



<a href="https://msdn.microsoft.com/070aac4e-94b6-4e23-b132-1dc833774c8b">IOleInPlaceSite::OnInPlaceDeactivate</a>



<a href="https://msdn.microsoft.com/926c02b4-0bfa-4509-b5bc-4e5007e4db1a">IOleInPlaceSite::OnUIDeactivate</a>



<a href="https://msdn.microsoft.com/61ecd153-ed6b-4a2c-a862-54742c5769ee">IOleObject::Close</a>
 

 

