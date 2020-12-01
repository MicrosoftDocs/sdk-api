---
UID: NF:winsync.ISyncChange.GetRootItemId
title: ISyncChange::GetRootItemId (winsync.h)
description: Gets the ID of the changed item.
helpviewer_keywords: ["GetRootItemId","GetRootItemId method [Windows Sync]","GetRootItemId method [Windows Sync]","ISyncChange interface","ISyncChange interface [Windows Sync]","GetRootItemId method","ISyncChange.GetRootItemId","ISyncChange::GetRootItemId","winsync.isyncchange_getrootitemid","winsync/ISyncChange::GetRootItemId"]
old-location: winsync\isyncchange_getrootitemid.htm
tech.root: winsync
ms.assetid: 775868d5-8cab-431a-913b-b22b2d516f0d
ms.date: 12/05/2018
ms.keywords: GetRootItemId, GetRootItemId method [Windows Sync], GetRootItemId method [Windows Sync],ISyncChange interface, ISyncChange interface [Windows Sync],GetRootItemId method, ISyncChange.GetRootItemId, ISyncChange::GetRootItemId, winsync.isyncchange_getrootitemid, winsync/ISyncChange::GetRootItemId
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
 - ISyncChange::GetRootItemId
 - winsync/ISyncChange::GetRootItemId
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
 - ISyncChange.GetRootItemId
---

# ISyncChange::GetRootItemId


## -description

Gets the ID of the changed item.

## -parameters

### -param pbRootItemId [in, out]

Returns the ID of the item.

### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbRootItemId</i>. Returns the number of bytes required to retrieve the ID when <i>pbRootItemId</i> is too small, or returns the number of bytes written.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbRootItemId</i> is too small. In this case, the required number of bytes is returned in <i>pcbIdSize</i>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange Interface</a>