---
UID: NF:winsync.IChangeConflict.GetResolveActionForChangeUnit
title: IChangeConflict::GetResolveActionForChangeUnit (winsync.h)
description: Gets the conflict resolution action for the conflicting change unit change.
helpviewer_keywords: ["GetResolveActionForChangeUnit","GetResolveActionForChangeUnit method [Windows Sync]","GetResolveActionForChangeUnit method [Windows Sync]","IChangeConflict interface","IChangeConflict interface [Windows Sync]","GetResolveActionForChangeUnit method","IChangeConflict.GetResolveActionForChangeUnit","IChangeConflict::GetResolveActionForChangeUnit","winsync.ichangeconflict_getresolveactionforchangeunit","winsync/IChangeConflict::GetResolveActionForChangeUnit"]
old-location: winsync\ichangeconflict_getresolveactionforchangeunit.htm
tech.root: winsync
ms.assetid: 206ee654-e8a6-4b71-b933-3380dc4ed0ad
ms.date: 12/05/2018
ms.keywords: GetResolveActionForChangeUnit, GetResolveActionForChangeUnit method [Windows Sync], GetResolveActionForChangeUnit method [Windows Sync],IChangeConflict interface, IChangeConflict interface [Windows Sync],GetResolveActionForChangeUnit method, IChangeConflict.GetResolveActionForChangeUnit, IChangeConflict::GetResolveActionForChangeUnit, winsync.ichangeconflict_getresolveactionforchangeunit, winsync/IChangeConflict::GetResolveActionForChangeUnit
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
 - IChangeConflict::GetResolveActionForChangeUnit
 - winsync/IChangeConflict::GetResolveActionForChangeUnit
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
 - IChangeConflict.GetResolveActionForChangeUnit
---

# IChangeConflict::GetResolveActionForChangeUnit


## -description

Gets the conflict resolution action for the conflicting change unit change.

## -parameters

### -param pChangeUnit [in]

The change unit for which to retrieve the conflict resolution action.

### -param pResolveAction [out]

The conflict resolution action that is specified for <i>pChangeUnit</i>.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeconflict">IChangeConflict Interface</a>



<a href="/windows/win32/api/winsync/ne-winsync-sync_resolve_action">SYNC RESOLVE ACTION Enumeration</a>