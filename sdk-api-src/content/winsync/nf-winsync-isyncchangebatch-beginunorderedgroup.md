---
UID: NF:winsync.ISyncChangeBatch.BeginUnorderedGroup
title: ISyncChangeBatch::BeginUnorderedGroup (winsync.h)
description: Opens an unordered group in the change batch. Item changes in this group can be in any order.
helpviewer_keywords: ["BeginUnorderedGroup","BeginUnorderedGroup method [Windows Sync]","BeginUnorderedGroup method [Windows Sync]","ISyncChangeBatch interface","ISyncChangeBatch interface [Windows Sync]","BeginUnorderedGroup method","ISyncChangeBatch.BeginUnorderedGroup","ISyncChangeBatch::BeginUnorderedGroup","winsync.isyncchangebatch_beginunorderedgroup","winsync/ISyncChangeBatch::BeginUnorderedGroup"]
old-location: winsync\isyncchangebatch_beginunorderedgroup.htm
tech.root: winsync
ms.assetid: 8d44451a-9150-4b2c-b126-d4fa90c2e192
ms.date: 12/05/2018
ms.keywords: BeginUnorderedGroup, BeginUnorderedGroup method [Windows Sync], BeginUnorderedGroup method [Windows Sync],ISyncChangeBatch interface, ISyncChangeBatch interface [Windows Sync],BeginUnorderedGroup method, ISyncChangeBatch.BeginUnorderedGroup, ISyncChangeBatch::BeginUnorderedGroup, winsync.isyncchangebatch_beginunorderedgroup, winsync/ISyncChangeBatch::BeginUnorderedGroup
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
 - ISyncChangeBatch::BeginUnorderedGroup
 - winsync/ISyncChangeBatch::BeginUnorderedGroup
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
 - ISyncChangeBatch.BeginUnorderedGroup
---

# ISyncChangeBatch::BeginUnorderedGroup


## -description

Opens an unordered group in the change batch. Item changes in this group can be in any order.



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
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
A group is already open or an empty group was previously added to the batch.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_CHANGE_BATCH_IS_READ_ONLY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -remarks

Item changes that are added to the change batch after this method is called are added to the open group.

Item changes cannot be added to the change batch until a group is opened.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch Interface</a>
