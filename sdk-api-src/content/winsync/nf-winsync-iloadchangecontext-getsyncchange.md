---
UID: NF:winsync.ILoadChangeContext.GetSyncChange
title: ILoadChangeContext::GetSyncChange (winsync.h)
description: Gets the change item for which the change data should be retrieved from the item store.
helpviewer_keywords: ["GetSyncChange","GetSyncChange method [Windows Sync]","GetSyncChange method [Windows Sync]","ILoadChangeContext interface","ILoadChangeContext interface [Windows Sync]","GetSyncChange method","ILoadChangeContext.GetSyncChange","ILoadChangeContext::GetSyncChange","winsync.iloadchangecontext_getsyncchange","winsync/ILoadChangeContext::GetSyncChange"]
old-location: winsync\iloadchangecontext_getsyncchange.htm
tech.root: winsync
ms.assetid: 6ac425bc-f6ec-4a95-b351-01f9eb27a744
ms.date: 12/05/2018
ms.keywords: GetSyncChange, GetSyncChange method [Windows Sync], GetSyncChange method [Windows Sync],ILoadChangeContext interface, ILoadChangeContext interface [Windows Sync],GetSyncChange method, ILoadChangeContext.GetSyncChange, ILoadChangeContext::GetSyncChange, winsync.iloadchangecontext_getsyncchange, winsync/ILoadChangeContext::GetSyncChange
req.header: winsync.h
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
 - ILoadChangeContext::GetSyncChange
 - winsync/ILoadChangeContext::GetSyncChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ILoadChangeContext.GetSyncChange
---

# ILoadChangeContext::GetSyncChange


## -description

Gets the change item for which the change data should be retrieved from the item store.

## -parameters

### -param ppSyncChange [out]

Returns the change item for which the change data should be retrieved from the item store.

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
<dt><b>SYNC_E_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
 When an internal error occurs.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iloadchangecontext">ILoadChangeContext Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynchronousdataretriever">ISynchronousDataRetriever Interface</a>