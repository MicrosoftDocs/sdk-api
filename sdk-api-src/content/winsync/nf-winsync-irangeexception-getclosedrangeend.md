---
UID: NF:winsync.IRangeException.GetClosedRangeEnd
title: IRangeException::GetClosedRangeEnd (winsync.h)
description: Gets the upper bound of the range of item IDs to exclude.
helpviewer_keywords: ["GetClosedRangeEnd","GetClosedRangeEnd method [Windows Sync]","GetClosedRangeEnd method [Windows Sync]","IRangeException interface","IRangeException interface [Windows Sync]","GetClosedRangeEnd method","IRangeException.GetClosedRangeEnd","IRangeException::GetClosedRangeEnd","winsync.irangeexception_getclosedrangeend","winsync/IRangeException::GetClosedRangeEnd"]
old-location: winsync\irangeexception_getclosedrangeend.htm
tech.root: winsync
ms.assetid: 1725d0b8-2ecb-4cce-b20f-7e8d0da502de
ms.date: 12/05/2018
ms.keywords: GetClosedRangeEnd, GetClosedRangeEnd method [Windows Sync], GetClosedRangeEnd method [Windows Sync],IRangeException interface, IRangeException interface [Windows Sync],GetClosedRangeEnd method, IRangeException.GetClosedRangeEnd, IRangeException::GetClosedRangeEnd, winsync.irangeexception_getclosedrangeend, winsync/IRangeException::GetClosedRangeEnd
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
 - IRangeException::GetClosedRangeEnd
 - winsync/IRangeException::GetClosedRangeEnd
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
 - IRangeException.GetClosedRangeEnd
---

# IRangeException::GetClosedRangeEnd


## -description

Gets the upper bound of the range of item IDs to exclude.

## -parameters

### -param pbClosedRangeEnd [in, out]

Returns the upper bound of the range of item IDs to exclude.

### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbClosedRangeEnd</i>. Returns the number of bytes required to retrieve the ID when <i>pbClosedRangeEnd</i> is too small, or returns the number of bytes written.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbClosedRangeEnd</i> is too small. In this case, the required number of bytes is returned in <i>pcbIdSize</i>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-irangeexception">IRangeException Interface</a>