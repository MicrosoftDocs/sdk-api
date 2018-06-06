---
UID: NF:syncregistration.ISyncProviderRegistration.RevokeEvent
title: ISyncProviderRegistration::RevokeEvent
author: windows-sdk-content
description: Unregisters the user from the notification of the arrival of new registration events.
old-location: winsync\isyncproviderregistration_revokeevent.htm
old-project: winsync
ms.assetid: fcc4901a-1507-461e-bbcc-a9e440ec05ce
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ISyncProviderRegistration interface [Windows Sync],RevokeEvent method, ISyncProviderRegistration.RevokeEvent, ISyncProviderRegistration::RevokeEvent, RevokeEvent, RevokeEvent method [Windows Sync], RevokeEvent method [Windows Sync],ISyncProviderRegistration interface, syncregistration/ISyncProviderRegistration::RevokeEvent, winsync.isyncproviderregistration_revokeevent
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
tech.root: 
req.typenames: SYNC_REGISTRATION_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - ISyncProviderRegistration.RevokeEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncProviderRegistration::RevokeEvent


## -description


Unregisters the user from the notification of the arrival of new registration
		events.


## -parameters




### -param hEvent [in]

The <b>HANDLE</b> returned by the <a href="https://msdn.microsoft.com/b636a3b4-2ac2-4400-b8ed-4430f598db7b">RegisterForEvent</a> method.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified event has not been registered.

</td>
</tr>
</table>
 




## -remarks



This method closes the specified <b>HANDLE</b> and cleans up any related memory.




## -see-also




<a href="https://msdn.microsoft.com/e7cf0c05-9d07-4630-ae34-9a9dd81492b2">ISyncProviderRegistration Interface</a>
 

 

