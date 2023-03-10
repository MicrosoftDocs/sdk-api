---
UID: NF:winsync.ISyncChangeBatch.EndUnorderedGroup
title: ISyncChangeBatch::EndUnorderedGroup (winsync.h)
description: Closes a previously opened unordered group in the change batch.
helpviewer_keywords: ["EndUnorderedGroup","EndUnorderedGroup method [Windows Sync]","EndUnorderedGroup method [Windows Sync]","ISyncChangeBatch interface","ISyncChangeBatch interface [Windows Sync]","EndUnorderedGroup method","ISyncChangeBatch.EndUnorderedGroup","ISyncChangeBatch::EndUnorderedGroup","winsync.isyncchangebatch_endunorderedgroup","winsync/ISyncChangeBatch::EndUnorderedGroup"]
old-location: winsync\isyncchangebatch_endunorderedgroup.htm
tech.root: winsync
ms.assetid: ca9c37ca-6aa0-437d-b933-ca7d943e4ef2
ms.date: 12/05/2018
ms.keywords: EndUnorderedGroup, EndUnorderedGroup method [Windows Sync], EndUnorderedGroup method [Windows Sync],ISyncChangeBatch interface, ISyncChangeBatch interface [Windows Sync],EndUnorderedGroup method, ISyncChangeBatch.EndUnorderedGroup, ISyncChangeBatch::EndUnorderedGroup, winsync.isyncchangebatch_endunorderedgroup, winsync/ISyncChangeBatch::EndUnorderedGroup
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
 - ISyncChangeBatch::EndUnorderedGroup
 - winsync/ISyncChangeBatch::EndUnorderedGroup
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
 - ISyncChangeBatch.EndUnorderedGroup
---

# ISyncChangeBatch::EndUnorderedGroup


## -description

Closes a previously opened unordered group in the change batch.

## -parameters

### -param pMadeWithKnowledge [in]

The made-with knowledge for the changes in the group. Typically, this is the knowledge of the replica that made this group.

### -param fAllChangesForKnowledge [in]

<b>TRUE</b> when all the changes contained in <i>pMadeWithKnowledge</i> are included in this change batch; otherwise, <b>FALSE</b>.

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
No group is open or an ordered group is open.

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

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>