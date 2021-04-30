---
UID: NF:syncregistration.ISyncProviderRegistration.UnregisterSyncProviderConfigUI
title: ISyncProviderRegistration::UnregisterSyncProviderConfigUI (syncregistration.h)
description: Unregisters and removes the specified synchronization provider configuration UI from the registration store.
helpviewer_keywords: ["ISyncProviderRegistration interface [Windows Sync]","UnregisterSyncProviderConfigUI method","ISyncProviderRegistration.UnregisterSyncProviderConfigUI","ISyncProviderRegistration::UnregisterSyncProviderConfigUI","UnregisterSyncProviderConfigUI","UnregisterSyncProviderConfigUI method [Windows Sync]","UnregisterSyncProviderConfigUI method [Windows Sync]","ISyncProviderRegistration interface","syncregistration/ISyncProviderRegistration::UnregisterSyncProviderConfigUI","winsync.isyncproviderregistration_unregistersyncproviderconfigui"]
old-location: winsync\isyncproviderregistration_unregistersyncproviderconfigui.htm
tech.root: winsync
ms.assetid: 14d0ab85-afd7-4615-8606-ec403a3dd453
ms.date: 12/05/2018
ms.keywords: ISyncProviderRegistration interface [Windows Sync],UnregisterSyncProviderConfigUI method, ISyncProviderRegistration.UnregisterSyncProviderConfigUI, ISyncProviderRegistration::UnregisterSyncProviderConfigUI, UnregisterSyncProviderConfigUI, UnregisterSyncProviderConfigUI method [Windows Sync], UnregisterSyncProviderConfigUI method [Windows Sync],ISyncProviderRegistration interface, syncregistration/ISyncProviderRegistration::UnregisterSyncProviderConfigUI, winsync.isyncproviderregistration_unregistersyncproviderconfigui
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
 - ISyncProviderRegistration::UnregisterSyncProviderConfigUI
 - syncregistration/ISyncProviderRegistration::UnregisterSyncProviderConfigUI
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
 - ISyncProviderRegistration.UnregisterSyncProviderConfigUI
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

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>



<a href="/windows/desktop/api/syncregistration/ns-syncregistration-syncproviderconfiguiconfiguration">SyncProviderConfigUIConfiguration Structure</a>