---
UID: NF:winsync.ISyncChangeBatchBase.AddItemMetadataToGroup
title: ISyncChangeBatchBase::AddItemMetadataToGroup (winsync.h)
description: Adds a specified item change to the group that is currently open.
helpviewer_keywords: ["AddItemMetadataToGroup","AddItemMetadataToGroup method [Windows Sync]","AddItemMetadataToGroup method [Windows Sync]","ISyncChangeBatchBase interface","ISyncChangeBatchBase interface [Windows Sync]","AddItemMetadataToGroup method","ISyncChangeBatchBase.AddItemMetadataToGroup","ISyncChangeBatchBase::AddItemMetadataToGroup","winsync.isyncchangebatchbase_additemmetadatatogroup","winsync/ISyncChangeBatchBase::AddItemMetadataToGroup"]
old-location: winsync\isyncchangebatchbase_additemmetadatatogroup.htm
tech.root: winsync
ms.assetid: cb5b5a35-70d9-413d-8bf6-7003fe7681c8
ms.date: 12/05/2018
ms.keywords: AddItemMetadataToGroup, AddItemMetadataToGroup method [Windows Sync], AddItemMetadataToGroup method [Windows Sync],ISyncChangeBatchBase interface, ISyncChangeBatchBase interface [Windows Sync],AddItemMetadataToGroup method, ISyncChangeBatchBase.AddItemMetadataToGroup, ISyncChangeBatchBase::AddItemMetadataToGroup, winsync.isyncchangebatchbase_additemmetadatatogroup, winsync/ISyncChangeBatchBase::AddItemMetadataToGroup
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
 - ISyncChangeBatchBase::AddItemMetadataToGroup
 - winsync/ISyncChangeBatchBase::AddItemMetadataToGroup
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
 - ISyncChangeBatchBase.AddItemMetadataToGroup
---

# ISyncChangeBatchBase::AddItemMetadataToGroup


## -description

Adds a specified item change to the group that is currently open.

## -parameters

### -param pbOwnerReplicaId [in]

The replica ID of the replica where <i>pChangeVersion</i> and <i>pCreationVersion</i> are valid. The ID format must match the format that is specified by the <a href="/windows/desktop/api/winsync/ns-winsync-id_parameters">ID_PARAMETERS</a> structure of the provider.

### -param pbItemId [in]

The ID of the item. The ID format must match the format that is specified by the <a href="/windows/desktop/api/winsync/ns-winsync-id_parameters">ID_PARAMETERS</a> structure of the provider.

### -param pChangeVersion [in]

The version of this change.

### -param pCreationVersion [in]

The creation version of the item.

### -param dwFlags [in]

Flags that specify the state of the item change. For the flag values, see <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchange-getflags">ISyncChange::GetFlags</a>.

### -param dwWorkForChange [in]

The work estimate for the change. This value is used during change application to report completed work to the application.

### -param ppChangeBuilder [in, out]

Returns an object that can be used to add change unit information to the change.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwFlags</i> contains a flag value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
No group is open or an empty group was previously added to the batch.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_RANGE_OUT_OF_ORDER</b></dt>
</dl>
</td>
<td width="60%">
An ordered group is open and <i>pbItemId</i> is less than the item ID of the previous item that was added to the group, or less than the item ID that was specified when the group was opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_CHANGE_BATCH_IS_READ_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The <b>ISyncChangeBatchBase</b> object has been sent to a change applier or to the synchronization session.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winsync/ns-winsync-id_parameters">ID_PARAMETERS Structure</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>



<a href="/windows/desktop/api/winsync/ns-winsync-sync_version">SYNC_VERSION Structure
</a>