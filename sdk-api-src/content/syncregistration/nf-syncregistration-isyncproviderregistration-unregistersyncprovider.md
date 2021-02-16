---
UID: NF:syncregistration.ISyncProviderRegistration.UnregisterSyncProvider
title: ISyncProviderRegistration::UnregisterSyncProvider (syncregistration.h)
description: Unregisters and removes the specified synchronization provider from the registration store.
helpviewer_keywords: ["ISyncProviderRegistration interface [Windows Sync]","UnregisterSyncProvider method","ISyncProviderRegistration.UnregisterSyncProvider","ISyncProviderRegistration::UnregisterSyncProvider","UnregisterSyncProvider","UnregisterSyncProvider method [Windows Sync]","UnregisterSyncProvider method [Windows Sync]","ISyncProviderRegistration interface","syncregistration/ISyncProviderRegistration::UnregisterSyncProvider","winsync.isyncproviderregistration_unregistersyncprovider"]
old-location: winsync\isyncproviderregistration_unregistersyncprovider.htm
tech.root: winsync
ms.assetid: d5b651b2-a0a5-404f-afbe-3256bf52f25f
ms.date: 12/05/2018
ms.keywords: ISyncProviderRegistration interface [Windows Sync],UnregisterSyncProvider method, ISyncProviderRegistration.UnregisterSyncProvider, ISyncProviderRegistration::UnregisterSyncProvider, UnregisterSyncProvider, UnregisterSyncProvider method [Windows Sync], UnregisterSyncProvider method [Windows Sync],ISyncProviderRegistration interface, syncregistration/ISyncProviderRegistration::UnregisterSyncProvider, winsync.isyncproviderregistration_unregistersyncprovider
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncProviderRegistration::UnregisterSyncProvider
 - syncregistration/ISyncProviderRegistration::UnregisterSyncProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - ISyncProviderRegistration.UnregisterSyncProvider
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

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>