---
UID: NF:syncregistration.ISyncProviderInfo.GetSyncProvider
title: ISyncProviderInfo::GetSyncProvider (syncregistration.h)
description: Creates an instance of the synchronization provider.
helpviewer_keywords: ["GetSyncProvider","GetSyncProvider method [Windows Sync]","GetSyncProvider method [Windows Sync]","ISyncProviderInfo interface","ISyncProviderInfo interface [Windows Sync]","GetSyncProvider method","ISyncProviderInfo.GetSyncProvider","ISyncProviderInfo::GetSyncProvider","syncregistration/ISyncProviderInfo::GetSyncProvider","winsync.isyncproviderinfo_getsyncprovider"]
old-location: winsync\isyncproviderinfo_getsyncprovider.htm
tech.root: winsync
ms.assetid: 74b70f31-0934-4599-9515-e94b6622d440
ms.date: 12/05/2018
ms.keywords: GetSyncProvider, GetSyncProvider method [Windows Sync], GetSyncProvider method [Windows Sync],ISyncProviderInfo interface, ISyncProviderInfo interface [Windows Sync],GetSyncProvider method, ISyncProviderInfo.GetSyncProvider, ISyncProviderInfo::GetSyncProvider, syncregistration/ISyncProviderInfo::GetSyncProvider, winsync.isyncproviderinfo_getsyncprovider
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
 - ISyncProviderInfo::GetSyncProvider
 - syncregistration/ISyncProviderInfo::GetSyncProvider
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
 - ISyncProviderInfo.GetSyncProvider
---

# ISyncProviderInfo::GetSyncProvider


## -description

Creates an instance of the synchronization provider.

## -parameters

### -param dwClsContext [in]

The context in which the code that manages the newly created object will run. The only context supported is <b>CLSCTX_INPROC_SERVER</b>.

### -param ppSyncProvider [out]

The instance of the synchronization provider.

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
There was not enough memory available to create the synchronization provider.

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

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderinfo">ISyncProviderInfo Interface</a>