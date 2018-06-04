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

# IOleInPlaceSiteEx::OnInPlaceActivateEx


## -description


Called by the embedded object to determine whether it needs to redraw itself upon activation.


## -parameters




### -param pfNoRedraw [out]

A pointer to a variable that receives the current redraw status. The status is <b>TRUE</b> if the object need not redraw itself upon activation and <b>FALSE</b> otherwise. Windowless objects usually do not need the value returned by this parameter and may pass a <b>NULL</b> pointer to save the container the burden of computing this value.


### -param dwFlags [in]

Indicates whether the object is activated as a windowless object. This parameter takes values from the <a href="https://msdn.microsoft.com/8748d3aa-3fea-4705-959c-3bc86b13a868">ACTIVATEFLAGS</a> enumeration. See <a href="https://msdn.microsoft.com/4ad83599-99d2-4b35-95de-cff845a8d5e4">IOleInPlaceSiteWindowless</a> for more information on windowless objects.


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



This method replaces <a href="https://msdn.microsoft.com/e5744911-1ea6-4482-988d-8def16229f4c">IOleInPlaceSite::OnInPlaceActivate</a>. If the older method is used, the object must always redraw itself on activation.

Windowless objects are required to use this method instead of <a href="https://msdn.microsoft.com/e5744911-1ea6-4482-988d-8def16229f4c">IOleInPlaceSite::OnInPlaceActivate</a> to notify the container of whether they are activating windowless or not.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The container should carefully check the invalidation status of the object, its z-order, clipping and any other relevant parameters to determine the appropriate value to return in <i>pfNoRedraw</i>.

A container can cache the value of the <a href="https://msdn.microsoft.com/8748d3aa-3fea-4705-959c-3bc86b13a868">ACTIVATEFLAGS</a> enumeration instead of calling the <a href="https://msdn.microsoft.com/833adc81-be58-44a1-88f1-9aa28808e67b">GetWindow</a> method in the <a href="https://msdn.microsoft.com/86aabb46-6bc7-4953-b4eb-8692552ca380">IOleInPlaceObjectWindowless</a> interface repeatedly.




## -see-also




<a href="https://msdn.microsoft.com/8748d3aa-3fea-4705-959c-3bc86b13a868">ACTIVATEFLAGS</a>



<a href="https://msdn.microsoft.com/86aabb46-6bc7-4953-b4eb-8692552ca380">IOleInPlaceObjectWindowless</a>



<a href="https://msdn.microsoft.com/e5744911-1ea6-4482-988d-8def16229f4c">IOleInPlaceSite::OnInPlaceActivate</a>



<a href="https://msdn.microsoft.com/d93e6d23-7867-43e4-8ab9-efe609362c18">IOleInPlaceSiteEx</a>



<a href="https://msdn.microsoft.com/4ad83599-99d2-4b35-95de-cff845a8d5e4">IOleInPlaceSiteWindowless</a>
 

 

