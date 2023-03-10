---
UID: NF:syncregistration.ISyncProviderRegistration.GetSyncProviderInfo
title: ISyncProviderRegistration::GetSyncProviderInfo (syncregistration.h)
description: Returns an ISyncProviderInfo object for the specific synchronization provider instance ID.
helpviewer_keywords: ["GetSyncProviderInfo","GetSyncProviderInfo method [Windows Sync]","GetSyncProviderInfo method [Windows Sync]","ISyncProviderRegistration interface","ISyncProviderRegistration interface [Windows Sync]","GetSyncProviderInfo method","ISyncProviderRegistration.GetSyncProviderInfo","ISyncProviderRegistration::GetSyncProviderInfo","syncregistration/ISyncProviderRegistration::GetSyncProviderInfo","winsync.isyncproviderregistration_getsyncproviderinfo"]
old-location: winsync\isyncproviderregistration_getsyncproviderinfo.htm
tech.root: winsync
ms.assetid: 894d2314-2210-4a16-a7e6-1ee74638c035
ms.date: 12/05/2018
ms.keywords: GetSyncProviderInfo, GetSyncProviderInfo method [Windows Sync], GetSyncProviderInfo method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],GetSyncProviderInfo method, ISyncProviderRegistration.GetSyncProviderInfo, ISyncProviderRegistration::GetSyncProviderInfo, syncregistration/ISyncProviderRegistration::GetSyncProviderInfo, winsync.isyncproviderregistration_getsyncproviderinfo
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
 - ISyncProviderRegistration::GetSyncProviderInfo
 - syncregistration/ISyncProviderRegistration::GetSyncProviderInfo
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
 - ISyncProviderRegistration.GetSyncProviderInfo
---

# ISyncProviderRegistration::GetSyncProviderInfo


## -description

Returns an <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderinfo">ISyncProviderInfo</a> object for the specific synchronization provider instance ID.

## -parameters

### -param pguidInstanceId [in]

The unique instance ID of the synchronization provider.

### -param ppProviderInfo [out]

The synchronization provider information object.

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
The specified instance ID does not match a registered synchronization provider.

</td>
</tr>
</table>

## -remarks

By calling the <a href="/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderinfo-getsyncprovider">GetSyncProvider</a> method of the <b>ISyncProviderInfo</b> object that is returned by this method,  you can get and set the properties of the synchronization provider, and  obtain the synchronization provider's <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-iregisteredsyncprovider">IRegisteredSyncProvider</a> instance.

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-iregisteredsyncprovider">IRegisteredSyncProvider Interface</a>



<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderinfo">ISyncProviderInfo Interface</a>



<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>