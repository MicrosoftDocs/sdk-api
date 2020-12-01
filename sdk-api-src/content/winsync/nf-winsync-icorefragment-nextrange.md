---
UID: NF:winsync.ICoreFragment.NextRange
title: ICoreFragment::NextRange (winsync.h)
description: Returns the next range that is contained in this knowledge fragment, and the clock vector that defines what is known about the items in the range.
helpviewer_keywords: ["ICoreFragment interface [Windows Sync]","NextRange method","ICoreFragment.NextRange","ICoreFragment::NextRange","NextRange","NextRange method [Windows Sync]","NextRange method [Windows Sync]","ICoreFragment interface","winsync.icorefragment_nextrange","winsync/ICoreFragment::NextRange"]
old-location: winsync\icorefragment_nextrange.htm
tech.root: winsync
ms.assetid: 25cfd4f5-2ff1-47eb-8cc0-17e17efa4ec2
ms.date: 12/05/2018
ms.keywords: ICoreFragment interface [Windows Sync],NextRange method, ICoreFragment.NextRange, ICoreFragment::NextRange, NextRange, NextRange method [Windows Sync], NextRange method [Windows Sync],ICoreFragment interface, winsync.icorefragment_nextrange, winsync/ICoreFragment::NextRange
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
 - ICoreFragment::NextRange
 - winsync/ICoreFragment::NextRange
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
 - ICoreFragment.NextRange
---

# ICoreFragment::NextRange


## -description

Returns the next range that is contained in this knowledge fragment, and the clock vector that defines what is known about the items in the range.

## -parameters

### -param pItemId [in, out]

Returns the closed lower bound of item IDs in this range. This value is also the open upper bound of item IDs in the previous range when it is not the first in the range set.

### -param pItemIdSize [in, out]

Specifies the number of bytes in <i>pItemId</i>. Returns the number of bytes written, or the number of bytes that are required to retrieve the ID when <i>pItemId</i> is too small.

### -param piClockVector [out]

Returns the clock vector that defines what is known about the items in the range.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no more ranges to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The item ID is a variable-length ID and <i>pItemIdSize</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pItemId</i> is too small. In this situation, the required number of bytes is returned in <i>pItemIdSize</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The knowledge object that is contained in this object has changed since this object was created.

</td>
</tr>
</table>

## -remarks

The value that is returned in <i>pItemId</i> is the closed lower bound on the range of item IDs that are associated with the clock vector that is returned in <i>piClockVector</i>. The value of <i>pItemId</i> also defines the open upper bound of the previous range, so the open upper bound of the current range can be obtained by calling <b>NextRange</b> again. If there are no more ranges to enumerate, the range contains all items that have IDs greater than or equal to <i>pItemId</i>.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-icorefragment">ICoreFragment Interface</a>