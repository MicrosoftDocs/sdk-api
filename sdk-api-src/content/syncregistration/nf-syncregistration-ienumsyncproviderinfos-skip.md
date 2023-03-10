---
UID: NF:syncregistration.IEnumSyncProviderInfos.Skip
title: IEnumSyncProviderInfos::Skip (syncregistration.h)
description: Skips the specified number of ISyncProviderInfo objects.
helpviewer_keywords: ["IEnumSyncProviderInfos interface [Windows Sync]","Skip method","IEnumSyncProviderInfos.Skip","IEnumSyncProviderInfos::Skip","Skip","Skip method [Windows Sync]","Skip method [Windows Sync]","IEnumSyncProviderInfos interface","syncregistration/IEnumSyncProviderInfos::Skip","winsync.ienumsyncproviderinfos_skip"]
old-location: winsync\ienumsyncproviderinfos_skip.htm
tech.root: winsync
ms.assetid: da59a26a-8df3-4a19-b771-6fd11f69576e
ms.date: 12/05/2018
ms.keywords: IEnumSyncProviderInfos interface [Windows Sync],Skip method, IEnumSyncProviderInfos.Skip, IEnumSyncProviderInfos::Skip, Skip, Skip method [Windows Sync], Skip method [Windows Sync],IEnumSyncProviderInfos interface, syncregistration/IEnumSyncProviderInfos::Skip, winsync.ienumsyncproviderinfos_skip
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
 - IEnumSyncProviderInfos::Skip
 - syncregistration/IEnumSyncProviderInfos::Skip
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
 - IEnumSyncProviderInfos.Skip
---

# IEnumSyncProviderInfos::Skip


## -description

Skips the specified number of <b>ISyncProviderInfo</b> objects.

## -parameters

### -param cInstances [in]

The number of <b>ISyncProviderInfo</b> objects to skip.

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

If the end of the collection is reached before the number of items to skip is reached, <b>S_FALSE</b> will be returned, and the enumerator will be placed at the end of the collection and subsequent calls to <b>Skip</b> or <a href="/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-ienumsyncproviderinfos-next">Next</a> with a count of 1 will return <b>S_FALSE</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-ienumsyncproviderinfos">IEnumSyncProviderInfos Interface</a>