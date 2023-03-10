---
UID: NF:winsync.ISyncFullEnumerationChangeBatch.GetClosedLowerBoundItemId
title: ISyncFullEnumerationChangeBatch::GetClosedLowerBoundItemId (winsync.h)
description: Gets the closed lower bound on item IDs that require destination versions.
helpviewer_keywords: ["GetClosedLowerBoundItemId","GetClosedLowerBoundItemId method [Windows Sync]","GetClosedLowerBoundItemId method [Windows Sync]","ISyncFullEnumerationChangeBatch interface","ISyncFullEnumerationChangeBatch interface [Windows Sync]","GetClosedLowerBoundItemId method","ISyncFullEnumerationChangeBatch.GetClosedLowerBoundItemId","ISyncFullEnumerationChangeBatch::GetClosedLowerBoundItemId","winsync.isyncfullenumerationchangebatch_getclosedlowerbounditemid","winsync/ISyncFullEnumerationChangeBatch::GetClosedLowerBoundItemId"]
old-location: winsync\isyncfullenumerationchangebatch_getclosedlowerbounditemid.htm
tech.root: winsync
ms.assetid: d0cc8564-f87a-4642-b085-5149c85279dd
ms.date: 12/05/2018
ms.keywords: GetClosedLowerBoundItemId, GetClosedLowerBoundItemId method [Windows Sync], GetClosedLowerBoundItemId method [Windows Sync],ISyncFullEnumerationChangeBatch interface, ISyncFullEnumerationChangeBatch interface [Windows Sync],GetClosedLowerBoundItemId method, ISyncFullEnumerationChangeBatch.GetClosedLowerBoundItemId, ISyncFullEnumerationChangeBatch::GetClosedLowerBoundItemId, winsync.isyncfullenumerationchangebatch_getclosedlowerbounditemid, winsync/ISyncFullEnumerationChangeBatch::GetClosedLowerBoundItemId
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
 - ISyncFullEnumerationChangeBatch::GetClosedLowerBoundItemId
 - winsync/ISyncFullEnumerationChangeBatch::GetClosedLowerBoundItemId
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
 - ISyncFullEnumerationChangeBatch.GetClosedLowerBoundItemId
---

# ISyncFullEnumerationChangeBatch::GetClosedLowerBoundItemId


## -description

Gets the closed lower bound on item IDs that require destination versions.

## -parameters

### -param pbClosedLowerBoundItemId [in, out]

Returns the closed lower bound on item IDs that require destination versions.

### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbClosedLowerBoundItemId</i>. Returns the number of bytes required for the size of <i>pbClosedLowerBoundItemId</i> when <i>pcbIdSize</i> is too small, or the number of bytes written to <i>pbClosedLowerBoundItemId</i>.

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
<i>pbClosedLowerBoundItemId</i> is too small. In this case, the required number of bytes is stored in <i>pcbIdSize</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
No group was added to the batch, or a group was opened but not ended.

</td>
</tr>
</table>

## -remarks

When the destination provider processes this change batch, it must provide version information for all its items that have item IDs that fall between the specified closed lower bound and closed upper bound, inclusive.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch Interface</a>