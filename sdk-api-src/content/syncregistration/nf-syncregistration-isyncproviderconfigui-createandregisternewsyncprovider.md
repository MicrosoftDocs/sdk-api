---
UID: NF:syncregistration.ISyncProviderConfigUI.CreateAndRegisterNewSyncProvider
title: ISyncProviderConfigUI::CreateAndRegisterNewSyncProvider (syncregistration.h)
description: Creates and registers a new synchronization provider.
helpviewer_keywords: ["CreateAndRegisterNewSyncProvider","CreateAndRegisterNewSyncProvider method [Windows Sync]","CreateAndRegisterNewSyncProvider method [Windows Sync]","ISyncProviderConfigUI interface","ISyncProviderConfigUI interface [Windows Sync]","CreateAndRegisterNewSyncProvider method","ISyncProviderConfigUI.CreateAndRegisterNewSyncProvider","ISyncProviderConfigUI::CreateAndRegisterNewSyncProvider","syncregistration/ISyncProviderConfigUI::CreateAndRegisterNewSyncProvider","winsync.isyncproviderconfigui_createandregisternewsyncprovider"]
old-location: winsync\isyncproviderconfigui_createandregisternewsyncprovider.htm
tech.root: winsync
ms.assetid: 4b256431-ed9a-414d-88c2-89f02000410d
ms.date: 12/05/2018
ms.keywords: CreateAndRegisterNewSyncProvider, CreateAndRegisterNewSyncProvider method [Windows Sync], CreateAndRegisterNewSyncProvider method [Windows Sync],ISyncProviderConfigUI interface, ISyncProviderConfigUI interface [Windows Sync],CreateAndRegisterNewSyncProvider method, ISyncProviderConfigUI.CreateAndRegisterNewSyncProvider, ISyncProviderConfigUI::CreateAndRegisterNewSyncProvider, syncregistration/ISyncProviderConfigUI::CreateAndRegisterNewSyncProvider, winsync.isyncproviderconfigui_createandregisternewsyncprovider
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
 - ISyncProviderConfigUI::CreateAndRegisterNewSyncProvider
 - syncregistration/ISyncProviderConfigUI::CreateAndRegisterNewSyncProvider
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
 - ISyncProviderConfigUI.CreateAndRegisterNewSyncProvider
---

# ISyncProviderConfigUI::CreateAndRegisterNewSyncProvider


## -description

Creates and registers a new  synchronization provider.

## -parameters

### -param hwndParent [in]

HWND serving as the parent for the configuration UI that needs to be presented before the synchronization provider can be created. 
    	The HWND should be <b>NULL</b> only if the <b>dwCapabilities</b> member of the <a href="/windows/win32/api/syncregistration/ns-syncregistration-syncproviderconfiguiconfiguration">SyncProviderConfigUIConfiguration</a> structure is set to not support a UI.

### -param pUnkContext [in]

Pointer to an interface containing additional information needed to generate the synchronization provider. The pointer will be <b>NULL</b> if no additional information is needed.

### -param ppProviderInfo [out]

An <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderinfo">ISyncProviderInfo</a> object that contains information about the newly created and registered synchronization provider.

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
There was not enough memory available to create and register the synchronization provider.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfigui">ISyncProviderConfigUI Interface</a>