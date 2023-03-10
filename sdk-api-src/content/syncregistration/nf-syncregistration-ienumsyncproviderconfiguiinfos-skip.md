---
UID: NF:syncregistration.IEnumSyncProviderConfigUIInfos.Skip
title: IEnumSyncProviderConfigUIInfos::Skip (syncregistration.h)
description: Skips the specified number of ISyncProviderConfigUIInfo objects.
helpviewer_keywords: ["IEnumSyncProviderConfigUIInfos interface [Windows Sync]","Skip method","IEnumSyncProviderConfigUIInfos.Skip","IEnumSyncProviderConfigUIInfos::Skip","Skip","Skip method [Windows Sync]","Skip method [Windows Sync]","IEnumSyncProviderConfigUIInfos interface","syncregistration/IEnumSyncProviderConfigUIInfos::Skip","winsync.ienumsyncproviderconfiguiinfos_skip"]
old-location: winsync\ienumsyncproviderconfiguiinfos_skip.htm
tech.root: winsync
ms.assetid: 7ecd6cce-77af-423a-9b95-80b1d7ec9d2f
ms.date: 12/05/2018
ms.keywords: IEnumSyncProviderConfigUIInfos interface [Windows Sync],Skip method, IEnumSyncProviderConfigUIInfos.Skip, IEnumSyncProviderConfigUIInfos::Skip, Skip, Skip method [Windows Sync], Skip method [Windows Sync],IEnumSyncProviderConfigUIInfos interface, syncregistration/IEnumSyncProviderConfigUIInfos::Skip, winsync.ienumsyncproviderconfiguiinfos_skip
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
 - IEnumSyncProviderConfigUIInfos::Skip
 - syncregistration/IEnumSyncProviderConfigUIInfos::Skip
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
 - IEnumSyncProviderConfigUIInfos.Skip
---

# IEnumSyncProviderConfigUIInfos::Skip


## -description

Skips the specified number of <b>ISyncProviderConfigUIInfo</b> objects.

## -parameters

### -param cFactories [in]

The number of <b>ISyncProviderConfigUIInfo</b> objects to skip.

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
The end of the collection was reached before the specified number of items was skipped.

</td>
</tr>
</table>

## -remarks

If the end of the collection is reached before the number of items to skip is reached, <b>S_FALSE</b> will be returned, and the enumerator will be placed at the end of the collection and subsequent calls to <b>Skip</b> or <a href="/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-ienumsyncproviderconfiguiinfos-next">Next</a> with a count of 1 will return <b>S_FALSE</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-ienumsyncproviderconfiguiinfos">IEnumSyncProviderConfigUIInfos Interface</a>