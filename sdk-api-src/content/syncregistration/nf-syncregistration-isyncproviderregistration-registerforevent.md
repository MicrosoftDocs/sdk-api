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

# ISyncProviderRegistration::RegisterForEvent


## -description


Registers the user to receive notification of the arrival of new registration
		events that oocur when changes are made to the registration store.


## -parameters




### -param phEvent [out]

A <b>HANDLE</b> to a synchronization event that is used to notify
		the caller about the arrival of new registration
		events.
		

<div class="alert"><b>Note</b>  The caller must not <b>Close</b> the returned <b>HANDLE</b>. The registration store will manage the memory for the <b>HANDLE</b> and will close it when the event is revoked by passing the <b>HANDLE</b> to  <a href="https://msdn.microsoft.com/fcc4901a-1507-461e-bbcc-a9e440ec05ce">RevokeEvent</a>, or before the store object is freed from memory.</div>
<div> </div>

## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>
 




## -remarks



The <b>HANDLE</b> returned by this method is used by the <a href="https://msdn.microsoft.com/6a65ba8b-b9cb-4d8c-8d18-9627547f9982">GetChange</a> method. The event will only be set once from the <b>RegisterForEvent</b> call.  Any subsequent notifications will only occur when the user calls the <b>GetChange</b> method.

To unregister from this event notification system, call the <a href="https://msdn.microsoft.com/fcc4901a-1507-461e-bbcc-a9e440ec05ce">RevokeEvent</a> method.




## -see-also




<a href="https://msdn.microsoft.com/e7cf0c05-9d07-4630-ae34-9a9dd81492b2">ISyncProviderRegistration Interface</a>
 

 

