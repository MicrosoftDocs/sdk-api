---
UID: NF:winsync.ISyncChangeBatch.AddLoggedConflict
title: ISyncChangeBatch::AddLoggedConflict (winsync.h)
description: Adds metadata that represents a conflict to the change batch.
helpviewer_keywords: ["AddLoggedConflict","AddLoggedConflict method [Windows Sync]","AddLoggedConflict method [Windows Sync]","ISyncChangeBatch interface","ISyncChangeBatch interface [Windows Sync]","AddLoggedConflict method","ISyncChangeBatch.AddLoggedConflict","ISyncChangeBatch::AddLoggedConflict","winsync.isyncchangebatch_addloggedconflict","winsync/ISyncChangeBatch::AddLoggedConflict"]
old-location: winsync\isyncchangebatch_addloggedconflict.htm
tech.root: winsync
ms.assetid: e7f83c35-754a-4211-b893-2df6f65266a6
ms.date: 12/05/2018
ms.keywords: AddLoggedConflict, AddLoggedConflict method [Windows Sync], AddLoggedConflict method [Windows Sync],ISyncChangeBatch interface, ISyncChangeBatch interface [Windows Sync],AddLoggedConflict method, ISyncChangeBatch.AddLoggedConflict, ISyncChangeBatch::AddLoggedConflict, winsync.isyncchangebatch_addloggedconflict, winsync/ISyncChangeBatch::AddLoggedConflict
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
 - ISyncChangeBatch::AddLoggedConflict
 - winsync/ISyncChangeBatch::AddLoggedConflict
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
 - ISyncChangeBatch.AddLoggedConflict
---

# ISyncChangeBatch::AddLoggedConflict


## -description

Adds metadata that represents a conflict to the change batch.

## -parameters

### -param pbOwnerReplicaId [in]

The ID of the replica that made the change in conflict.

### -param pbItemId [in]

The ID of the item.

### -param pChangeVersion [in]

The version of the change.

### -param pCreationVersion [in]

The creation version of the item.

### -param dwFlags [in]

Flags that specify the state of the item change. For the SYNC_CHANGE_FLAG values, see the Remarks section of the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchange-getflags">ISyncChange::GetFlags</a> method.

### -param dwWorkForChange [in]

The work estimate for the change. This value is used during change application to report completed work to the application.

### -param pConflictKnowledge [in]

The conflict knowledge that was saved when the conflict was logged.

### -param ppChangeBuilder [out]

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%"></td>
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

Conflicts that are added to the change batch are not added to a group. A group does not have to be opened to add conflicts to the change batch.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncChange Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebuilder">ISyncChangeBuilder Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>