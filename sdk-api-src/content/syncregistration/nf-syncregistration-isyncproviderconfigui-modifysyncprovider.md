---
UID: NF:syncregistration.ISyncProviderConfigUI.ModifySyncProvider
title: ISyncProviderConfigUI::ModifySyncProvider (syncregistration.h)
description: Updates the ISyncProviderInfo of the synchronization provider that is configured by this ISyncProviderConfigUI.
helpviewer_keywords: ["ISyncProviderConfigUI interface [Windows Sync]","ModifySyncProvider method","ISyncProviderConfigUI.ModifySyncProvider","ISyncProviderConfigUI::ModifySyncProvider","ModifySyncProvider","ModifySyncProvider method [Windows Sync]","ModifySyncProvider method [Windows Sync]","ISyncProviderConfigUI interface","syncregistration/ISyncProviderConfigUI::ModifySyncProvider","winsync.isyncproviderconfigui_modifysyncprovider"]
old-location: winsync\isyncproviderconfigui_modifysyncprovider.htm
tech.root: winsync
ms.assetid: 16f6d30c-422a-4638-a63b-f9d2a5fdb8b4
ms.date: 12/05/2018
ms.keywords: ISyncProviderConfigUI interface [Windows Sync],ModifySyncProvider method, ISyncProviderConfigUI.ModifySyncProvider, ISyncProviderConfigUI::ModifySyncProvider, ModifySyncProvider, ModifySyncProvider method [Windows Sync], ModifySyncProvider method [Windows Sync],ISyncProviderConfigUI interface, syncregistration/ISyncProviderConfigUI::ModifySyncProvider, winsync.isyncproviderconfigui_modifysyncprovider
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
 - ISyncProviderConfigUI::ModifySyncProvider
 - syncregistration/ISyncProviderConfigUI::ModifySyncProvider
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
 - ISyncProviderConfigUI.ModifySyncProvider
---

# ISyncProviderConfigUI::ModifySyncProvider


## -description

Updates the <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderinfo">ISyncProviderInfo</a> of the synchronization provider that is configured by this <b>ISyncProviderConfigUI</b>.

## -parameters

### -param hwndParent [in]

HWND serving as the parent for the configuration UI that needs to be presented before the synchronization provider can be created. 
    	The HWND should be <b>NULL</b> only if the <b>dwCapabilities</b> member of the <a href="/windows/win32/api/syncregistration/ns-syncregistration-syncproviderconfiguiconfiguration">SyncProviderConfigUIConfiguration</a> structure is set to not support a UI.

### -param pUnkContext [in]

Pointer to an interface containing additional information needed to generate the synchronization provider. The pointer will be <b>NULL</b> if no additional information is needed.

### -param pProviderInfo [in]

An <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderinfo">ISyncProviderInfo</a> that provides information about the synchronization provider that is being modified.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfigui">ISyncProviderConfigUI Interface</a>