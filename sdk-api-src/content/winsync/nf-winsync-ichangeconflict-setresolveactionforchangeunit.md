---
UID: NF:winsync.IChangeConflict.SetResolveActionForChangeUnit
title: IChangeConflict::SetResolveActionForChangeUnit (winsync.h)
description: Sets a conflict resolution action for the conflicting change unit change.
helpviewer_keywords: ["IChangeConflict interface [Windows Sync]","SetResolveActionForChangeUnit method","IChangeConflict.SetResolveActionForChangeUnit","IChangeConflict::SetResolveActionForChangeUnit","SetResolveActionForChangeUnit","SetResolveActionForChangeUnit method [Windows Sync]","SetResolveActionForChangeUnit method [Windows Sync]","IChangeConflict interface","winsync.ichangeconflict_setresolveactionforchangeunit","winsync/IChangeConflict::SetResolveActionForChangeUnit"]
old-location: winsync\ichangeconflict_setresolveactionforchangeunit.htm
tech.root: winsync
ms.assetid: 8594a888-21a1-4cfb-964c-9c670e3a7438
ms.date: 12/05/2018
ms.keywords: IChangeConflict interface [Windows Sync],SetResolveActionForChangeUnit method, IChangeConflict.SetResolveActionForChangeUnit, IChangeConflict::SetResolveActionForChangeUnit, SetResolveActionForChangeUnit, SetResolveActionForChangeUnit method [Windows Sync], SetResolveActionForChangeUnit method [Windows Sync],IChangeConflict interface, winsync.ichangeconflict_setresolveactionforchangeunit, winsync/IChangeConflict::SetResolveActionForChangeUnit
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
 - IChangeConflict::SetResolveActionForChangeUnit
 - winsync/IChangeConflict::SetResolveActionForChangeUnit
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
 - IChangeConflict.SetResolveActionForChangeUnit
---

# IChangeConflict::SetResolveActionForChangeUnit


## -description

Sets a conflict resolution action for the conflicting change unit change.

## -parameters

### -param pChangeUnit [in]

The change unit for which to set the conflict resolution action.

### -param resolveAction [in]

The conflict resolution action to set for <i>pChangeUnit</i>.

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
<dt><b>SYNC_E_INTERNAL_ERROR </b></dt>
</dl>
</td>
<td width="60%">
When the conflict is an update-delete conflict, or when no conflict exists.

</td>
</tr>
</table>

## -remarks

Be aware that setting the conflict resolution action for a change unit on an update-delete conflict is not valid, because this type of conflict must be resolved at the item level.

By setting this action in an event handler for <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onconflict">ISyncCallback::OnConflict</a>, the event handler specifies how the change applier should handle the conflict.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeconflict">IChangeConflict Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onconflict">ISyncCallback::OnConflict Method</a>



<a href="/windows/win32/api/winsync/ne-winsync-sync_resolve_action">SYNC RESOLVE ACTION Enumeration</a>