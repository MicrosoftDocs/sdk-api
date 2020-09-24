---
UID: NF:syncregistration.ISyncProviderRegistration.EnumerateSyncProviders
title: ISyncProviderRegistration::EnumerateSyncProviders (syncregistration.h)
description: Returns an IEnumSyncProviderInfos enumeration interface that enumerates all registered ISyncProviderInfo objects for the specified criteria.
helpviewer_keywords: ["EnumerateSyncProviders","EnumerateSyncProviders method [Windows Sync]","EnumerateSyncProviders method [Windows Sync]","ISyncProviderRegistration interface","ISyncProviderRegistration interface [Windows Sync]","EnumerateSyncProviders method","ISyncProviderRegistration.EnumerateSyncProviders","ISyncProviderRegistration::EnumerateSyncProviders","syncregistration/ISyncProviderRegistration::EnumerateSyncProviders","winsync.isyncproviderregistration_enumeratesyncproviders"]
old-location: winsync\isyncproviderregistration_enumeratesyncproviders.htm
tech.root: winsync
ms.assetid: 36a2b498-237e-418a-b5b8-5f9bcdfbe734
ms.date: 12/05/2018
ms.keywords: EnumerateSyncProviders, EnumerateSyncProviders method [Windows Sync], EnumerateSyncProviders method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],EnumerateSyncProviders method, ISyncProviderRegistration.EnumerateSyncProviders, ISyncProviderRegistration::EnumerateSyncProviders, syncregistration/ISyncProviderRegistration::EnumerateSyncProviders, winsync.isyncproviderregistration_enumeratesyncproviders
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
 - ISyncProviderRegistration::EnumerateSyncProviders
 - syncregistration/ISyncProviderRegistration::EnumerateSyncProviders
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
 - ISyncProviderRegistration.EnumerateSyncProviders
---

# ISyncProviderRegistration::EnumerateSyncProviders


## -description

Returns an <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-ienumsyncproviderinfos">IEnumSyncProviderInfos</a> enumeration interface that enumerates all registered <b>ISyncProviderInfo</b> objects for the specified  criteria.

## -parameters

### -param pguidContentType [in]

The LPCGUID of the specified content type. If this parameter is <b>NULL</b>, all content types will be enumerated.

### -param dwStateFlagsToFilterMask [in]

A synchronization provider state flag that can be used to mask (preserve or remove) the existing state. If this parameter is set to zero, all synchronization provider states will be enumerated. See the <i>dwStateFlagsToFilter</i> parameter description for a list of flags.

### -param dwStateFlagsToFilter [in]

One of the following flags that represent the synchronization provider state.

<ul>
<li><b>SYNC_PROVIDER_STATE_ENABLED</b>  ((DWORD)0x00000001)The provider is enabled and available for synchronization.

</li>
<li><b>SYNC_PROVIDER_STATE_DIRTY</b>  ((DWORD)0x00000002)The active provider has been updated and has new data to synchronize.

</li>
</ul>
If this parameter is set to zero, all synchronization provider states will be enumerated.

### -param refProviderClsId [in]

The REFCLSID of a particular provider. If this parameter is set to <b>CLSID_NULL</b>, all providers will be enumerated.

### -param dwSupportedArchitecture [in]

One, or a combination  of, the following flags that represent the architectures of the providers to be enumerated. If <b>SYNC_32_BIT_SUPPORTED</b> is specified, all providers that support 32 bits or 32 and 64 bits will be enumerated.  If <b>SYNC_32_BIT_SUPPORTED</b> | <b>SYNC_64_BIT_SUPPORTED</b> is specified, only those providers that support both 32 bits and 64 bits will be enumerated.

<ul>
<li><b>SYNC_32_BIT_SUPPORTED</b> ((DWORD)0x00000001)</li>
<li><b>SYNC_64_BIT_SUPPORTED</b>  ((DWORD)0x00000002)</li>
</ul>
If this parameter is set to zero, synchronization providers for all architectures will be enumerated.

### -param ppEnumSyncProviderInfos [out]

The <b>IEnumSyncProviderInfos</b> enumeration interface that will enumerate all <b>ISyncProviderInfo</b> objects that match the specified criteria.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory available to return the enumeration interface.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-ienumsyncproviderinfos">IEnumSyncProviderInfos Interface</a>



<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>