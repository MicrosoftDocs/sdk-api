---
UID: NF:syncregistration.ISyncProviderRegistration.CreateSyncProviderRegistrationInstance
title: ISyncProviderRegistration::CreateSyncProviderRegistrationInstance (syncregistration.h)
description: Creates an in-memory instance of a synchronization provider.
helpviewer_keywords: ["CreateSyncProviderRegistrationInstance","CreateSyncProviderRegistrationInstance method [Windows Sync]","CreateSyncProviderRegistrationInstance method [Windows Sync]","ISyncProviderRegistration interface","ISyncProviderRegistration interface [Windows Sync]","CreateSyncProviderRegistrationInstance method","ISyncProviderRegistration.CreateSyncProviderRegistrationInstance","ISyncProviderRegistration::CreateSyncProviderRegistrationInstance","syncregistration/ISyncProviderRegistration::CreateSyncProviderRegistrationInstance","winsync.isyncproviderregistration_createsyncproviderregistrationinstance"]
old-location: winsync\isyncproviderregistration_createsyncproviderregistrationinstance.htm
tech.root: winsync
ms.assetid: 637cf465-5d43-42d3-b7b9-3bd674135038
ms.date: 12/05/2018
ms.keywords: CreateSyncProviderRegistrationInstance, CreateSyncProviderRegistrationInstance method [Windows Sync], CreateSyncProviderRegistrationInstance method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],CreateSyncProviderRegistrationInstance method, ISyncProviderRegistration.CreateSyncProviderRegistrationInstance, ISyncProviderRegistration::CreateSyncProviderRegistrationInstance, syncregistration/ISyncProviderRegistration::CreateSyncProviderRegistrationInstance, winsync.isyncproviderregistration_createsyncproviderregistrationinstance
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
 - ISyncProviderRegistration::CreateSyncProviderRegistrationInstance
 - syncregistration/ISyncProviderRegistration::CreateSyncProviderRegistrationInstance
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
 - ISyncProviderRegistration.CreateSyncProviderRegistrationInstance
---

# ISyncProviderRegistration::CreateSyncProviderRegistrationInstance


## -description

Creates an in-memory instance of a synchronization provider.

## -parameters

### -param pProviderConfiguration [in]

A <a href="/windows/win32/api/syncregistration/ns-syncregistration-syncproviderconfiguration">SyncProviderConfiguration</a> structure that contains the synchronization provider registration information.

### -param ppProviderInfo [out]

Returns a pointer to an <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderinfo">ISyncProviderInfo</a> interface that is used to obtain information about the synchronization provider and access the configuration property store in order to store the synchronization provider configuration.

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
<dt><b>SYNC_E_REGISTRATION_ALREADYREGISTERED </b></dt>
</dl>
</td>
<td width="60%">
The same unique instance ID has already been registered for a synchronization provider.

</td>
</tr>
</table>

## -remarks

The synchronization provider is not registered on the system until the <b>ISyncProviderInfo::Commit</b> method is called. This method is inherited by <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderinfo">ISyncProviderInfo</a> from <b>IPropertyStore</b>. For an example of this, see <a href="/previous-versions/windows/desktop/winsync/overview-of-registering-a-synchronization-provider">Overview of Registering a Synchronization Provider</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>



<a href="/windows/win32/api/syncregistration/ns-syncregistration-syncproviderconfiguration">SyncProviderConfiguration Structure</a>