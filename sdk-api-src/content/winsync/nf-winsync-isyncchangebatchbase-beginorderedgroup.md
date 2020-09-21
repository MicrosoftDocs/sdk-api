---
UID: NF:winsync.ISyncChangeBatchBase.BeginOrderedGroup
title: ISyncChangeBatchBase::BeginOrderedGroup (winsync.h)
description: Opens an ordered group in the change batch. This group is ordered by item ID.
helpviewer_keywords: ["BeginOrderedGroup","BeginOrderedGroup method [Windows Sync]","BeginOrderedGroup method [Windows Sync]","ISyncChangeBatchBase interface","ISyncChangeBatchBase interface [Windows Sync]","BeginOrderedGroup method","ISyncChangeBatchBase.BeginOrderedGroup","ISyncChangeBatchBase::BeginOrderedGroup","winsync.isyncchangebatchbase_beginorderedgroup","winsync/ISyncChangeBatchBase::BeginOrderedGroup"]
old-location: winsync\isyncchangebatchbase_beginorderedgroup.htm
tech.root: winsync
ms.assetid: 093c0014-fa03-4609-a38f-5e69a3d3c4d6
ms.date: 12/05/2018
ms.keywords: BeginOrderedGroup, BeginOrderedGroup method [Windows Sync], BeginOrderedGroup method [Windows Sync],ISyncChangeBatchBase interface, ISyncChangeBatchBase interface [Windows Sync],BeginOrderedGroup method, ISyncChangeBatchBase.BeginOrderedGroup, ISyncChangeBatchBase::BeginOrderedGroup, winsync.isyncchangebatchbase_beginorderedgroup, winsync/ISyncChangeBatchBase::BeginOrderedGroup
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
 - ISyncChangeBatchBase::BeginOrderedGroup
 - winsync/ISyncChangeBatchBase::BeginOrderedGroup
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
 - ISyncChangeBatchBase.BeginOrderedGroup
---

# ISyncChangeBatchBase::BeginOrderedGroup


## -description

Opens an ordered group in the change batch. This group is ordered by item ID.

## -parameters

### -param pbLowerBound [in]

The closed lower bound of item IDs for this ordered group. To specify a lower bound of zero, use <b>NULL</b>.

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
<td width="60%">
The object is an <b>ISyncFullEnumerationChangeBatch</b>  object and a group has already been added to the batch. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_RANGE_OUT_OF_ORDER</b></dt>
</dl>
</td>
<td width="60%">
The object is an <b>ISyncFullEnumerationChangeBatch</b> object and <i>pbLowerBound</i> is greater than the lower bound ID that was used to create the batch.

</td>
</tr>
</table>

## -remarks

Item changes that are added to the change batch after this method is called are added to the open group. Item changes that are added to an ordered group must be added in increasing order by item ID.

Item changes cannot be added to the change batch until a group is opened.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>