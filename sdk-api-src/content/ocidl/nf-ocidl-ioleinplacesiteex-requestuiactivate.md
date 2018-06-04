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

# IOleInPlaceSiteEx::RequestUIActivate


## -description


Notifies the container that the object is about to enter the UI-active state.


## -parameters






## -returns



This method returns S_OK if the object can continue the activation process and call <a href="https://msdn.microsoft.com/d863805c-58c1-4e35-84b5-72f01a4ba205">IOleInPlaceSite::OnUIActivate</a>. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object cannot enter the UI-active state. The object must call <a href="https://msdn.microsoft.com/926c02b4-0bfa-4509-b5bc-4e5007e4db1a">IOleInPlaceSite::OnUIDeactivate</a> so the container can perform its the necessary processing to restore the focus.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
</table>
 




## -remarks



An object calls this method to determine if it can enter the UI-active state and to notify the container that it is about to make this transition. The container can return S_FALSE to deny this request, for example, if the end user has canceled the operation or if the currently active object will not relinquish its active state.

If the object does not call <b>IOleInPlaceSiteEx::RequestUIActivate</b>, the container handles data validation and fires Enter and Exit events from <a href="https://msdn.microsoft.com/d863805c-58c1-4e35-84b5-72f01a4ba205">IOleInPlaceSite::OnUIActivate</a>.




## -see-also




<a href="https://msdn.microsoft.com/d863805c-58c1-4e35-84b5-72f01a4ba205">IOleInPlaceSite::OnUIActivate</a>



<a href="https://msdn.microsoft.com/926c02b4-0bfa-4509-b5bc-4e5007e4db1a">IOleInPlaceSite::OnUIDeactivate</a>



<a href="https://msdn.microsoft.com/d93e6d23-7867-43e4-8ab9-efe609362c18">IOleInPlaceSiteEx</a>
 

 

