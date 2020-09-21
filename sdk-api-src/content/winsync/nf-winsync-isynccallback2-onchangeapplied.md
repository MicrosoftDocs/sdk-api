---
UID: NF:winsync.ISyncCallback2.OnChangeApplied
title: ISyncCallback2::OnChangeApplied (winsync.h)
description: Occurs after a change is successfully applied.
helpviewer_keywords: ["ISyncCallback2 interface [Windows Sync]","OnChangeApplied method","ISyncCallback2.OnChangeApplied","ISyncCallback2::OnChangeApplied","OnChangeApplied","OnChangeApplied method [Windows Sync]","OnChangeApplied method [Windows Sync]","ISyncCallback2 interface","winsync.isynccallback2_onchangeapplied","winsync/ISyncCallback2::OnChangeApplied"]
old-location: winsync\isynccallback2_onchangeapplied.htm
tech.root: winsync
ms.assetid: 3397ca51-583b-4051-892b-68f505d85ccd
ms.date: 12/05/2018
ms.keywords: ISyncCallback2 interface [Windows Sync],OnChangeApplied method, ISyncCallback2.OnChangeApplied, ISyncCallback2::OnChangeApplied, OnChangeApplied, OnChangeApplied method [Windows Sync], OnChangeApplied method [Windows Sync],ISyncCallback2 interface, winsync.isynccallback2_onchangeapplied, winsync/ISyncCallback2::OnChangeApplied
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
 - ISyncCallback2::OnChangeApplied
 - winsync/ISyncCallback2::OnChangeApplied
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
 - ISyncCallback2.OnChangeApplied
---

# ISyncCallback2::OnChangeApplied


## -description

Occurs after a change is successfully applied.

## -parameters

### -param dwChangesApplied [in]

The number of changes that have been successfully applied during the synchronization session. This value is the sum of item changes plus change unit changes.

### -param dwChangesFailed [in]

The number of changes that have failed to apply during the synchronization session. This value is the sum of item changes plus change unit changes.

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
<dt><b>Application-determined error codes</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback">ISyncCallback Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback2">ISyncCallback2 Interface</a>