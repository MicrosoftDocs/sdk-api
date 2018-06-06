---
UID: NF:syncregistration.ISyncProviderRegistration.UnregisterSyncProvider
title: ISyncProviderRegistration::UnregisterSyncProvider
author: windows-sdk-content
description: Unregisters and removes the specified synchronization provider from the registration store.
old-location: winsync\isyncproviderregistration_unregistersyncprovider.htm
old-project: winsync
ms.assetid: d5b651b2-a0a5-404f-afbe-3256bf52f25f
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ISyncProviderRegistration interface [Windows Sync],UnregisterSyncProvider method, ISyncProviderRegistration.UnregisterSyncProvider, ISyncProviderRegistration::UnregisterSyncProvider, UnregisterSyncProvider, UnregisterSyncProvider method [Windows Sync], UnregisterSyncProvider method [Windows Sync],ISyncProviderRegistration interface, syncregistration/ISyncProviderRegistration::UnregisterSyncProvider, winsync.isyncproviderregistration_unregistersyncprovider
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
 - ISyncProviderRegistration.UnregisterSyncProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncProviderRegistration::UnregisterSyncProvider


## -description


Unregisters and removes the specified synchronization provider from the registration store.


## -parameters




### -param pguidInstanceId [in]

The unique instance ID of the synchronization provider.


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
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_REGISTRATION_NOTREGISTERED  </b></dt>
</dl>
</td>
<td width="60%">
A synchronization provider with the specified instance ID is not currently registered.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e7cf0c05-9d07-4630-ae34-9a9dd81492b2">ISyncProviderRegistration Interface</a>
 

 

