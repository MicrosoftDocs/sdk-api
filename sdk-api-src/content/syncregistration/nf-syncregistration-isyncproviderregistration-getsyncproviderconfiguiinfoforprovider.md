---
UID: NF:syncregistration.ISyncProviderRegistration.GetSyncProviderConfigUIInfoforProvider
title: ISyncProviderRegistration::GetSyncProviderConfigUIInfoforProvider (syncregistration.h)
description: Returns an ISyncProviderConfigUIInfo object for the specified synchronization provider instance ID.
helpviewer_keywords: ["GetSyncProviderConfigUIInfoforProvider","GetSyncProviderConfigUIInfoforProvider method [Windows Sync]","GetSyncProviderConfigUIInfoforProvider method [Windows Sync]","ISyncProviderRegistration interface","ISyncProviderRegistration interface [Windows Sync]","GetSyncProviderConfigUIInfoforProvider method","ISyncProviderRegistration.GetSyncProviderConfigUIInfoforProvider","ISyncProviderRegistration::GetSyncProviderConfigUIInfoforProvider","syncregistration/ISyncProviderRegistration::GetSyncProviderConfigUIInfoforProvider","winsync.isyncproviderregistration_getsyncproviderconfiguiinfoforprovider"]
old-location: winsync\isyncproviderregistration_getsyncproviderconfiguiinfoforprovider.htm
tech.root: winsync
ms.assetid: 6ef774f8-0b97-44ee-8bb9-7adf2293cc23
ms.date: 12/05/2018
ms.keywords: GetSyncProviderConfigUIInfoforProvider, GetSyncProviderConfigUIInfoforProvider method [Windows Sync], GetSyncProviderConfigUIInfoforProvider method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],GetSyncProviderConfigUIInfoforProvider method, ISyncProviderRegistration.GetSyncProviderConfigUIInfoforProvider, ISyncProviderRegistration::GetSyncProviderConfigUIInfoforProvider, syncregistration/ISyncProviderRegistration::GetSyncProviderConfigUIInfoforProvider, winsync.isyncproviderregistration_getsyncproviderconfiguiinfoforprovider
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
 - ISyncProviderRegistration::GetSyncProviderConfigUIInfoforProvider
 - syncregistration/ISyncProviderRegistration::GetSyncProviderConfigUIInfoforProvider
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
 - ISyncProviderRegistration.GetSyncProviderConfigUIInfoforProvider
---

# ISyncProviderRegistration::GetSyncProviderConfigUIInfoforProvider


## -description

Returns an <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfiguiinfo">ISyncProviderConfigUIInfo</a> object for the specified synchronization provider instance ID.

## -parameters

### -param pguidProviderInstanceId [in]

The unique instance ID of the synchronization provider.

### -param ppProviderConfigUIInfo [out]

The configuration UI information object.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No configuration UI was specified for the synchronization provider.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory available to return the synchronization provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_REGISTRATION_NOTREGISTERED  </b></dt>
</dl>
</td>
<td width="60%">
The specified instance ID does not match a registered synchronization provider, or the requested configuration UI is not registered.

</td>
</tr>
</table>

## -remarks

This method is used to get and set the configuration UI properties for the specified  synchronization provider and to obtain the <b>ISyncProviderConfigUI</b> instance.

This method is used to obtain an <b>ISyncProviderConfigUIInfo</b> object when the instance ID is not known, but the instance ID of the  synchronization provider is known. The <a href="/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-getsyncproviderconfiguifrominstanceid">GetSyncProviderConfigUIFromInstanceId</a> method should be used if you want to access an <b>ISyncProviderConfigUIInfo</b> object directly using the instance ID of an <b>ISyncProviderConfigUI</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfigui">ISyncProviderConfigUI Interface</a>



<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfiguiinfo">ISyncProviderConfigUIInfo Interface</a>



<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>