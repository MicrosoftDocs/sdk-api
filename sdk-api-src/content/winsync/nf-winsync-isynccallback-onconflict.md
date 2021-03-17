---
UID: NF:winsync.ISyncCallback.OnConflict
title: ISyncCallback::OnConflict (winsync.h)
description: Occurs when a conflict is detected when the concurrency conflict resolution policy is set to CRP_NONE.
helpviewer_keywords: ["ISyncCallback interface [Windows Sync]","OnConflict method","ISyncCallback.OnConflict","ISyncCallback::OnConflict","OnConflict","OnConflict method [Windows Sync]","OnConflict method [Windows Sync]","ISyncCallback interface","winsync.isynccallback_onconflict","winsync/ISyncCallback::OnConflict"]
old-location: winsync\isynccallback_onconflict.htm
tech.root: winsync
ms.assetid: 439f2a73-b36c-4604-b739-9f9b68275ac5
ms.date: 12/05/2018
ms.keywords: ISyncCallback interface [Windows Sync],OnConflict method, ISyncCallback.OnConflict, ISyncCallback::OnConflict, OnConflict, OnConflict method [Windows Sync], OnConflict method [Windows Sync],ISyncCallback interface, winsync.isynccallback_onconflict, winsync/ISyncCallback::OnConflict
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
 - ISyncCallback::OnConflict
 - winsync/ISyncCallback::OnConflict
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
 - ISyncCallback.OnConflict
---

# ISyncCallback::OnConflict


## -description

Occurs when a conflict is detected when the concurrency conflict resolution policy is set to <a href="/windows/win32/api/winsync/ne-winsync-conflict_resolution_policy">CRP_NONE</a>.

## -parameters

### -param pConflict [in]

Information about the conflict. This includes metadata and item data for the two changes that are in conflict.

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
<dt><b>Application-determined error codes.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -remarks

This notification can be used by an application to perform custom conflict resolution for concurrency conflicts. To accomplish this, the application inspects and processes the contents of <i>pConflict</i>, and then sets the resolution action for the conflict by calling <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeconflict">IChangeConflict::SetResolveActionForChange</a> before it returns from this method.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeconflict">IChangeConflict Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback">ISyncCallback Interface</a>



<a href="/windows/win32/api/winsync/ne-winsync-sync_full_enumeration_action">SYNC_FULL_ENUMERATION_ACTION Enumeration</a>