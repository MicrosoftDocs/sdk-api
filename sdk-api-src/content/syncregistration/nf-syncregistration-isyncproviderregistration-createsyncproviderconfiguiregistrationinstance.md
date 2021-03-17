---
UID: NF:syncregistration.ISyncProviderRegistration.CreateSyncProviderConfigUIRegistrationInstance
title: ISyncProviderRegistration::CreateSyncProviderConfigUIRegistrationInstance (syncregistration.h)
description: Creates an in-memory instance of a synchronization provider configuration UI.
helpviewer_keywords: ["CreateSyncProviderConfigUIRegistrationInstance","CreateSyncProviderConfigUIRegistrationInstance method [Windows Sync]","CreateSyncProviderConfigUIRegistrationInstance method [Windows Sync]","ISyncProviderRegistration interface","ISyncProviderRegistration interface [Windows Sync]","CreateSyncProviderConfigUIRegistrationInstance method","ISyncProviderRegistration.CreateSyncProviderConfigUIRegistrationInstance","ISyncProviderRegistration::CreateSyncProviderConfigUIRegistrationInstance","syncregistration/ISyncProviderRegistration::CreateSyncProviderConfigUIRegistrationInstance","winsync.isyncproviderregistration_createsyncproviderconfiguiregistrationinstance"]
old-location: winsync\isyncproviderregistration_createsyncproviderconfiguiregistrationinstance.htm
tech.root: winsync
ms.assetid: a61b07b3-45ce-429e-9641-4cebc5b44c1b
ms.date: 12/05/2018
ms.keywords: CreateSyncProviderConfigUIRegistrationInstance, CreateSyncProviderConfigUIRegistrationInstance method [Windows Sync], CreateSyncProviderConfigUIRegistrationInstance method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],CreateSyncProviderConfigUIRegistrationInstance method, ISyncProviderRegistration.CreateSyncProviderConfigUIRegistrationInstance, ISyncProviderRegistration::CreateSyncProviderConfigUIRegistrationInstance, syncregistration/ISyncProviderRegistration::CreateSyncProviderConfigUIRegistrationInstance, winsync.isyncproviderregistration_createsyncproviderconfiguiregistrationinstance
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
 - ISyncProviderRegistration::CreateSyncProviderConfigUIRegistrationInstance
 - syncregistration/ISyncProviderRegistration::CreateSyncProviderConfigUIRegistrationInstance
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
 - ISyncProviderRegistration.CreateSyncProviderConfigUIRegistrationInstance
---

# ISyncProviderRegistration::CreateSyncProviderConfigUIRegistrationInstance


## -description

Creates an in-memory instance of a synchronization provider configuration UI.

## -parameters

### -param pConfigUIConfig [in]

A <a href="/windows/win32/api/syncregistration/ns-syncregistration-syncproviderconfiguiconfiguration">SyncProviderConfigUIConfiguration</a> structure that contains the configuration UI registration information.

### -param ppConfigUIInfo [out]

  Returns a pointer to an <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfiguiinfo">ISyncProviderConfigUIInfo</a> interface that is used to store the configuration UI’s UX elements and any necessary persisted configuration information.

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
The same CLSID and content type combination, or the same unique instance ID has already been registered for a configuration UI.

</td>
</tr>
</table>

## -remarks

The configuration UI is not registered on the system until the <b>ISyncProviderConfigUIInfo::Commit</b> method is called. This method is inherited by <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfiguiinfo">ISyncProviderConfigUIInfo</a> from <b>IPropertyStore</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>



<a href="/windows/win32/api/syncregistration/ns-syncregistration-syncproviderconfiguiconfiguration">SyncProviderConfigUIConfiguration Structure</a>