---
UID: NF:oleidl.IOleInPlaceSite.Scroll
title: IOleInPlaceSite::Scroll
author: windows-sdk-content
description: Instructs the container to scroll the view of the object by the specified number of pixels.
old-location: com\ioleinplacesite_scroll.htm
tech.root: com
ms.assetid: a169c4c6-b600-4812-bf71-d7fcd7486ff1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOleInPlaceSite interface [COM],Scroll method, IOleInPlaceSite.Scroll, IOleInPlaceSite::Scroll, IOleInPlaceSiteWindowless.Scroll, Scroll, Scroll method [COM], Scroll method [COM],IOleInPlaceSite interface, _ole_ioleinplacesite_scroll, com.ioleinplacesite_scroll, oleidl/IOleInPlaceSite::Scroll
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
 - IOleInPlaceSite.Scroll
 - IOleInPlaceSiteWindowless.Scroll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

