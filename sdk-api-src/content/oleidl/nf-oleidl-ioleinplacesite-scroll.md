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

# IOleInPlaceSite::Scroll


## -description


Instructs the container to scroll the view of the object by the specified number of pixels.


## -parameters




### -param scrollExtant [in]

The number of pixels by which to scroll in the X and Y directions.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified pointer is not valid.

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



As a result of scrolling, the object's visible rectangle can change. If that happens, the container should give the new clipping rectangle to the object by calling <a href="https://msdn.microsoft.com/5ae2e44b-d2e2-4351-b4fa-8c37419a2bcb">IOleInPlaceObject::SetObjectRects</a>. The intersection of the <i>lprcClipRect</i> and <i>lprcPosRect</i> rectangles gives the new visible rectangle. See <a href="https://msdn.microsoft.com/f6cf62b3-5a64-49aa-b0bd-56744ecee313">IOleInPlaceSite::GetWindowContext</a> for more information.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Called by an active, in-place object when it is asking the container to scroll.




## -see-also




<a href="https://msdn.microsoft.com/5ae2e44b-d2e2-4351-b4fa-8c37419a2bcb">IOleInPlaceObject::SetObjectRects</a>



<a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>
 

 

