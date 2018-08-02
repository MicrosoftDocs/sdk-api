---
UID: NF:syncregistration.ISyncProviderRegistration.UnregisterSyncProviderConfigUI
title: ISyncProviderRegistration::UnregisterSyncProviderConfigUI
author: windows-sdk-content
description: Unregisters and removes the specified synchronization provider configuration UI from the registration store.
old-location: winsync\isyncproviderregistration_unregistersyncproviderconfigui.htm
old-project: winsync
ms.assetid: 14d0ab85-afd7-4615-8606-ec403a3dd453
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISyncProviderRegistration interface [Windows Sync],UnregisterSyncProviderConfigUI method, ISyncProviderRegistration.UnregisterSyncProviderConfigUI, ISyncProviderRegistration::UnregisterSyncProviderConfigUI, UnregisterSyncProviderConfigUI, UnregisterSyncProviderConfigUI method [Windows Sync], UnregisterSyncProviderConfigUI method [Windows Sync],ISyncProviderRegistration interface, syncregistration/ISyncProviderRegistration::UnregisterSyncProviderConfigUI, winsync.isyncproviderregistration_unregistersyncproviderconfigui
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
 - ISyncProviderRegistration.UnregisterSyncProviderConfigUI
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncProviderRegistration::UnregisterSyncProviderConfigUI


## -description


Unregisters and removes the specified synchronization provider configuration UI from the registration store.


## -parameters




### -param pguidInstanceId [in]

The unique instance ID of the synchronization provider configuration UI.


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
The CLSID and content type combination does not exist in the registration store for a configuration UI.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e7cf0c05-9d07-4630-ae34-9a9dd81492b2">ISyncProviderRegistration Interface</a>



<a href="https://msdn.microsoft.com/4f07719b-c1e5-4985-a952-0ff07601bf1a">SyncProviderConfigUIConfiguration Structure</a>
 

 

