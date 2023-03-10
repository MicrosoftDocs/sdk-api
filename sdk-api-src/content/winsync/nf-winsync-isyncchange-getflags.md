---
UID: NF:winsync.ISyncChange.GetFlags
title: ISyncChange::GetFlags (winsync.h)
description: Gets flags that are associated with this change.
helpviewer_keywords: ["GetFlags","GetFlags method [Windows Sync]","GetFlags method [Windows Sync]","ISyncChange interface","ISyncChange interface [Windows Sync]","GetFlags method","ISyncChange.GetFlags","ISyncChange::GetFlags","winsync.isyncchange_getflags","winsync/ISyncChange::GetFlags"]
old-location: winsync\isyncchange_getflags.htm
tech.root: winsync
ms.assetid: de0509a4-550b-49f2-a850-fc1bd57b60cd
ms.date: 12/05/2018
ms.keywords: GetFlags, GetFlags method [Windows Sync], GetFlags method [Windows Sync],ISyncChange interface, ISyncChange interface [Windows Sync],GetFlags method, ISyncChange.GetFlags, ISyncChange::GetFlags, winsync.isyncchange_getflags, winsync/ISyncChange::GetFlags
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
 - ISyncChange::GetFlags
 - winsync/ISyncChange::GetFlags
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
 - ISyncChange.GetFlags
---

# ISyncChange::GetFlags


## -description

Gets flags that are associated with this change.

## -parameters

### -param pdwFlags [out]

Returns the flags that are associated with this change. This will be a combination of <b>SYNC_CHANGE_FLAG</b> values (See Remarks).

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

## -remarks

The following table describes the values that the source and destination provider can use for this property.

<table>
<tr>
<th>SYNC_CHANGE_FLAG value </th>
<th>Provider </th>
<th>Indicates </th>
</tr>
<tr>
<td><b>SYNC_CHANGE_FLAG_DELETED 
</b></td>
<td>Source or destination
</td>
<td>The item previously existed in the replica but has been deleted.
</td>
</tr>
<tr>
<td><b>SYNC_CHANGE_FLAG_DOES_NOT_EXIST</b></td>
<td>Destination only
</td>
<td>The item does not exist in the destination replica.
</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange Interface</a>