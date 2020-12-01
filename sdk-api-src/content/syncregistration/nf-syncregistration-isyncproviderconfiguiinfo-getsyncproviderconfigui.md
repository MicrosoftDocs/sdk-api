---
UID: NF:syncregistration.ISyncProviderConfigUIInfo.GetSyncProviderConfigUI
title: ISyncProviderConfigUIInfo::GetSyncProviderConfigUI (syncregistration.h)
description: Creates an instance of a synchronization provider configuration UI.
helpviewer_keywords: ["GetSyncProviderConfigUI","GetSyncProviderConfigUI method [Windows Sync]","GetSyncProviderConfigUI method [Windows Sync]","ISyncProviderConfigUIInfo interface","ISyncProviderConfigUIInfo interface [Windows Sync]","GetSyncProviderConfigUI method","ISyncProviderConfigUIInfo.GetSyncProviderConfigUI","ISyncProviderConfigUIInfo::GetSyncProviderConfigUI","syncregistration/ISyncProviderConfigUIInfo::GetSyncProviderConfigUI","winsync.isyncproviderconfiguiinfo_getsyncproviderconfigui"]
old-location: winsync\isyncproviderconfiguiinfo_getsyncproviderconfigui.htm
tech.root: winsync
ms.assetid: eb9a2f2f-4c9f-405c-90f6-b251ab1a652d
ms.date: 12/05/2018
ms.keywords: GetSyncProviderConfigUI, GetSyncProviderConfigUI method [Windows Sync], GetSyncProviderConfigUI method [Windows Sync],ISyncProviderConfigUIInfo interface, ISyncProviderConfigUIInfo interface [Windows Sync],GetSyncProviderConfigUI method, ISyncProviderConfigUIInfo.GetSyncProviderConfigUI, ISyncProviderConfigUIInfo::GetSyncProviderConfigUI, syncregistration/ISyncProviderConfigUIInfo::GetSyncProviderConfigUI, winsync.isyncproviderconfiguiinfo_getsyncproviderconfigui
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
 - ISyncProviderConfigUIInfo::GetSyncProviderConfigUI
 - syncregistration/ISyncProviderConfigUIInfo::GetSyncProviderConfigUI
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
 - ISyncProviderConfigUIInfo.GetSyncProviderConfigUI
---

# ISyncProviderConfigUIInfo::GetSyncProviderConfigUI


## -description

Creates an instance of a synchronization provider configuration UI.

## -parameters

### -param dwClsContext [in]

The context in which the code that manages the newly created object will run. The only context supported is <b>CLSCTX_INPROC_SERVER</b>.

### -param ppSyncProviderConfigUI [out]

The instance of the synchronization provider configuration UI.

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
There was not enough memory available to create the configuration UI.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_DATA)</b></dt>
</dl>
</td>
<td width="60%">
Information stored in the registration store is an unexpected size.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfiguiinfo">ISyncProviderConfigUIInfo Interface</a>