---
UID: NF:syncregistration.ISyncProviderRegistration.GetSyncProviderState
title: ISyncProviderRegistration::GetSyncProviderState (syncregistration.h)
description: Returns the state of the specified synchronization provider.
helpviewer_keywords: ["GetSyncProviderState","GetSyncProviderState method [Windows Sync]","GetSyncProviderState method [Windows Sync]","ISyncProviderRegistration interface","ISyncProviderRegistration interface [Windows Sync]","GetSyncProviderState method","ISyncProviderRegistration.GetSyncProviderState","ISyncProviderRegistration::GetSyncProviderState","syncregistration/ISyncProviderRegistration::GetSyncProviderState","winsync.isyncproviderregistration_getsyncproviderstate"]
old-location: winsync\isyncproviderregistration_getsyncproviderstate.htm
tech.root: winsync
ms.assetid: 4e2e2e17-e435-4def-9aee-9109e0e06a8c
ms.date: 12/05/2018
ms.keywords: GetSyncProviderState, GetSyncProviderState method [Windows Sync], GetSyncProviderState method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],GetSyncProviderState method, ISyncProviderRegistration.GetSyncProviderState, ISyncProviderRegistration::GetSyncProviderState, syncregistration/ISyncProviderRegistration::GetSyncProviderState, winsync.isyncproviderregistration_getsyncproviderstate
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
 - ISyncProviderRegistration::GetSyncProviderState
 - syncregistration/ISyncProviderRegistration::GetSyncProviderState
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
 - ISyncProviderRegistration.GetSyncProviderState
---

# ISyncProviderRegistration::GetSyncProviderState


## -description

Returns the state of the specified synchronization provider.

## -parameters

### -param pguidInstanceId [in]

The unique instance ID of the synchronization provider.

### -param pdwStateFlags [out]

One of the following flags that represent the synchronization provider state.

<ul>
<li><b>SYNC_PROVIDER_STATE_ENABLED</b>  ((DWORD)0x00000001)The provider is enabled and available for synchronization.

</li>
<li><b>SYNC_PROVIDER_STATE_DIRTY</b>  ((DWORD)0x00000002)The active provider has been updated and has new data to synchronize.

</li>
</ul>

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
A synchronization provider with the specified instance ID was not registered.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>