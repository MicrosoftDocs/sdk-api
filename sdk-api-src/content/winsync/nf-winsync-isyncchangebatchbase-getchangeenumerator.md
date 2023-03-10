---
UID: NF:winsync.ISyncChangeBatchBase.GetChangeEnumerator
title: ISyncChangeBatchBase::GetChangeEnumerator (winsync.h)
description: Gets an IEnumSyncChanges object that enumerates the item changes in this change batch.
helpviewer_keywords: ["GetChangeEnumerator","GetChangeEnumerator method [Windows Sync]","GetChangeEnumerator method [Windows Sync]","ISyncChangeBatchBase interface","ISyncChangeBatchBase interface [Windows Sync]","GetChangeEnumerator method","ISyncChangeBatchBase.GetChangeEnumerator","ISyncChangeBatchBase::GetChangeEnumerator","winsync.isyncchangebatchbase_getchangeenumerator","winsync/ISyncChangeBatchBase::GetChangeEnumerator"]
old-location: winsync\isyncchangebatchbase_getchangeenumerator.htm
tech.root: winsync
ms.assetid: af979d71-1eb4-463d-8e90-27a985ea289d
ms.date: 12/05/2018
ms.keywords: GetChangeEnumerator, GetChangeEnumerator method [Windows Sync], GetChangeEnumerator method [Windows Sync],ISyncChangeBatchBase interface, ISyncChangeBatchBase interface [Windows Sync],GetChangeEnumerator method, ISyncChangeBatchBase.GetChangeEnumerator, ISyncChangeBatchBase::GetChangeEnumerator, winsync.isyncchangebatchbase_getchangeenumerator, winsync/ISyncChangeBatchBase::GetChangeEnumerator
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
 - ISyncChangeBatchBase::GetChangeEnumerator
 - winsync/ISyncChangeBatchBase::GetChangeEnumerator
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
 - ISyncChangeBatchBase.GetChangeEnumerator
---

# ISyncChangeBatchBase::GetChangeEnumerator


## -description

Gets an <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ienumsyncchanges">IEnumSyncChanges</a> object that enumerates the item changes in this change batch.

## -parameters

### -param ppEnum [out]

Returns an enumerator that contains the item changes in this change batch.

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
<dt><b>E_POINTER

</b></dt>
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
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ienumsyncchanges">IEnumSyncChanges Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>