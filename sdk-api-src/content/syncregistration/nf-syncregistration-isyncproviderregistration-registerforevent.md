---
UID: NF:syncregistration.ISyncProviderRegistration.RegisterForEvent
title: ISyncProviderRegistration::RegisterForEvent
author: windows-sdk-content
description: Registers the user to receive notification of the arrival of new registration events that oocur when changes are made to the registration store.
old-location: winsync\isyncproviderregistration_registerforevent.htm
old-project: winsync
ms.assetid: b636a3b4-2ac2-4400-b8ed-4430f598db7b
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ISyncProviderRegistration interface [Windows Sync],RegisterForEvent method, ISyncProviderRegistration.RegisterForEvent, ISyncProviderRegistration::RegisterForEvent, RegisterForEvent, RegisterForEvent method [Windows Sync], RegisterForEvent method [Windows Sync],ISyncProviderRegistration interface, syncregistration/ISyncProviderRegistration::RegisterForEvent, winsync.isyncproviderregistration_registerforevent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: syncregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SYNC_REGISTRATION_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncregistration.h
api_name:
-	ISyncProviderRegistration.RegisterForEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

