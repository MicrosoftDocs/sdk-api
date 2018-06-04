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

# IOleInPlaceSiteEx::OnInPlaceDeactivateEx


## -description


Notifies the container if the object needs to be redrawn upon deactivation.


## -parameters




### -param fNoRedraw [in]

If <b>TRUE</b>, the container need not redraw the object after completing the deactivation; if <b>FALSE</b> the object must be redrawn after deactivation.


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



This method replaces <a href="https://msdn.microsoft.com/070aac4e-94b6-4e23-b132-1dc833774c8b">IOleInPlaceSite::OnInPlaceDeactivate</a>. If the older method is used, the object must always be redrawn on deactivation.




## -see-also




<a href="https://msdn.microsoft.com/070aac4e-94b6-4e23-b132-1dc833774c8b">IOleInPlaceSite::OnInPlaceDeactivate</a>



<a href="https://msdn.microsoft.com/d93e6d23-7867-43e4-8ab9-efe609362c18">IOleInPlaceSiteEx</a>
 

 

