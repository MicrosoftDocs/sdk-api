---
UID: NF:oleidl.IOleInPlaceSite.OnInPlaceDeactivate
title: IOleInPlaceSite::OnInPlaceDeactivate method
author: windows-driver-content
description: Notifies the container that the object is no longer active in place.
old-location: com\ioleinplacesite_oninplacedeactivate.htm
old-project: com
ms.assetid: 070aac4e-94b6-4e23-b132-1dc833774c8b
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IOleInPlaceSite, IOleInPlaceSite interface [COM], OnInPlaceDeactivate method, IOleInPlaceSite::OnInPlaceDeactivate, OnInPlaceDeactivate method [COM], OnInPlaceDeactivate method [COM], IOleInPlaceSite interface, OnInPlaceDeactivate,IOleInPlaceSite.OnInPlaceDeactivate, _ole_ioleinplacesite_oninplacedeactivate, com.ioleinplacesite_oninplacedeactivate, oleidl/IOleInPlaceSite::OnInPlaceDeactivate
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
-	browsewm.dll
api_name:
-	IOleInPlaceSite.OnInPlaceDeactivate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOleInPlaceSite::OnInPlaceDeactivate method


## -description


Notifies the container that the object is no longer active in place.


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
<b>OnInPlaceDeactivate</b> is called by an in-place object when it is fully deactivated. This function notifies the container that the object has been deactivated, and it gives the container a chance to run code pertinent to the object's deactivation. In particular, <b>OnInPlaceDeactivate</b> is called as a result of <a href="https://msdn.microsoft.com/174a8bde-0795-4d4d-a294-7708c7d1823a">IOleInPlaceObject::InPlaceDeactivate</a> being called. Calling <b>OnInPlaceDeactivate</b> indicates that the object can no longer support Undo.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the container is holding pointers to the <a href="https://msdn.microsoft.com/c14de79d-e844-49cf-ae70-6c3e417fab90">IOleInPlaceObject</a> and <a href="https://msdn.microsoft.com/b077c256-1109-494c-95c2-2d33bccbe47b">IOleInPlaceActiveObject</a> interface implementations, it should release them after the <b>OnInPlaceDeactivate</b> call.




## -see-also




<a href="https://msdn.microsoft.com/174a8bde-0795-4d4d-a294-7708c7d1823a">IOleInPlaceObject::InPlaceDeactivate</a>



<a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>
 

 

