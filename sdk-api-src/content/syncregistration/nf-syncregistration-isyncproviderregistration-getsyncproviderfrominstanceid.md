---
UID: NF:syncregistration.ISyncProviderRegistration.GetSyncProviderFromInstanceId
title: ISyncProviderRegistration::GetSyncProviderFromInstanceId (syncregistration.h)
description: Returns an initialized and instantiated IRegisteredSyncProvider object for the specific unique instance ID.
helpviewer_keywords: ["GetSyncProviderFromInstanceId","GetSyncProviderFromInstanceId method [Windows Sync]","GetSyncProviderFromInstanceId method [Windows Sync]","ISyncProviderRegistration interface","ISyncProviderRegistration interface [Windows Sync]","GetSyncProviderFromInstanceId method","ISyncProviderRegistration.GetSyncProviderFromInstanceId","ISyncProviderRegistration::GetSyncProviderFromInstanceId","syncregistration/ISyncProviderRegistration::GetSyncProviderFromInstanceId","winsync.isyncproviderregistration_getsyncproviderfrominstanceid"]
old-location: winsync\isyncproviderregistration_getsyncproviderfrominstanceid.htm
tech.root: winsync
ms.assetid: ed204998-9e9a-4bac-b178-b4137be87ff4
ms.date: 12/05/2018
ms.keywords: GetSyncProviderFromInstanceId, GetSyncProviderFromInstanceId method [Windows Sync], GetSyncProviderFromInstanceId method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],GetSyncProviderFromInstanceId method, ISyncProviderRegistration.GetSyncProviderFromInstanceId, ISyncProviderRegistration::GetSyncProviderFromInstanceId, syncregistration/ISyncProviderRegistration::GetSyncProviderFromInstanceId, winsync.isyncproviderregistration_getsyncproviderfrominstanceid
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
 - ISyncProviderRegistration::GetSyncProviderFromInstanceId
 - syncregistration/ISyncProviderRegistration::GetSyncProviderFromInstanceId
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
 - ISyncProviderRegistration.GetSyncProviderFromInstanceId
---

# ISyncProviderRegistration::GetSyncProviderFromInstanceId


## -description

Returns an initialized and instantiated  <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-iregisteredsyncprovider">IRegisteredSyncProvider</a> object for the specific unique instance ID.

## -parameters

### -param pguidInstanceId [in]

The unique instance ID of the <b>IRegisteredSyncProvider</b> object.

### -param dwClsContext [in]

The context in which the code that manages the newly created object will run. The only context supported is <b>CLSCTX_INPROC_SERVER</b>.

### -param ppSyncProvider [out]

The initialized and instantiated synchronization provider object.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The instance ID is <b>GUID_NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory available to create the synchronization provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The synchronization provider’s CLSID is not registered with the requested context or the provider has not had its DLL registered.

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

## -remarks

<div class="alert"><b>Note</b>  The caller of this method should not explicitly call <b>IRegisteredSyncProvider::Init</b> on the <b>IRegisteredSyncProvider</b> object that is returned, as this method will do this on the caller's behalf. The caller should call <b>QueryInterface</b> on the <b>IRegisteredSyncProvider</b> object that is returned to obtain an <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncprovider">ISyncProvider</a> interface to pass to the synchronization session.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-iregisteredsyncprovider">IRegisteredSyncProvider Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncprovider">ISyncProvider Interface</a>



<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>