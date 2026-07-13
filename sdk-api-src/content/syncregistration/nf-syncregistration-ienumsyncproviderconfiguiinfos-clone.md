---
UID: NF:syncregistration.IEnumSyncProviderConfigUIInfos.Clone
title: IEnumSyncProviderConfigUIInfos::Clone (syncregistration.h)
description: Clones the enumerator and returns a new enumerator that is in the same state as the current one. (IEnumSyncProviderConfigUIInfos.Clone)
helpviewer_keywords: ["Clone","Clone method [Windows Sync]","Clone method [Windows Sync]","IEnumSyncProviderConfigUIInfos interface","IEnumSyncProviderConfigUIInfos interface [Windows Sync]","Clone method","IEnumSyncProviderConfigUIInfos.Clone","IEnumSyncProviderConfigUIInfos::Clone","syncregistration/IEnumSyncProviderConfigUIInfos::Clone","winsync.ienumsyncproviderconfiguiinfos_clone"]
old-location: winsync\ienumsyncproviderconfiguiinfos_clone.htm
tech.root: winsync
ms.assetid: 30f2a85a-86c2-4547-a18f-448a01d64d9b
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Sync], Clone method [Windows Sync],IEnumSyncProviderConfigUIInfos interface, IEnumSyncProviderConfigUIInfos interface [Windows Sync],Clone method, IEnumSyncProviderConfigUIInfos.Clone, IEnumSyncProviderConfigUIInfos::Clone, syncregistration/IEnumSyncProviderConfigUIInfos::Clone, winsync.ienumsyncproviderconfiguiinfos_clone
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
 - IEnumSyncProviderConfigUIInfos::Clone
 - syncregistration/IEnumSyncProviderConfigUIInfos::Clone
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
 - IEnumSyncProviderConfigUIInfos.Clone
---

# IEnumSyncProviderConfigUIInfos::Clone


## -description

Clones the enumerator and returns a new enumerator that is in the same state as the current one.

## -parameters

### -param ppEnum [out]

Returns the newly cloned enumerator.

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
There was not enough memory available to clone the enumerator.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-ienumsyncproviderconfiguiinfos">IEnumSyncProviderConfigUIInfos Interface</a>
