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

# ITCallNotificationEvent::get_Event


## -description


The 
<b>get_Event</b> method returns a 
<a href="https://msdn.microsoft.com/0c05042f-af1e-4657-bb1c-e6741361b11c">CALL_NOTIFICATION_EVENT</a> description of whether the application owns or is monitoring the call on which the event has occurred.


## -parameters




### -param pCallNotificationEvent [out]

Pointer to the 
<a href="https://msdn.microsoft.com/0c05042f-af1e-4657-bb1c-e6741361b11c">CALL_NOTIFICATION_EVENT</a> description of the application's privilege on the call returned by 
<a href="https://msdn.microsoft.com/6ff82bd1-de69-4ab7-9152-a578b8566755">ITCallNotificationEvent::get_Call</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCallNotificationEvent</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0c05042f-af1e-4657-bb1c-e6741361b11c">CALL_NOTIFICATION_EVENT</a>



<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/d0ea4f7a-7b50-4610-ae17-957c0c1891e1">ITCallNotificationEvent</a>
 

 

