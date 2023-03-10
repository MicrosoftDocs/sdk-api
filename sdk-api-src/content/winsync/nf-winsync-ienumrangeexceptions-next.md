---
UID: NF:winsync.IEnumRangeExceptions.Next
title: IEnumRangeExceptions::Next (winsync.h)
description: Returns the next elements in the change unit exception set, if they are available. (IEnumRangeExceptions.Next)
helpviewer_keywords: ["IEnumRangeExceptions interface [Windows Sync]","Next method","IEnumRangeExceptions.Next","IEnumRangeExceptions::Next","Next","Next method [Windows Sync]","Next method [Windows Sync]","IEnumRangeExceptions interface","winsync.ienumrangeexceptions_next","winsync/IEnumRangeExceptions::Next"]
old-location: winsync\ienumrangeexceptions_next.htm
tech.root: winsync
ms.assetid: 0ca472d7-4e97-4998-b883-05329dfdb27a
ms.date: 12/05/2018
ms.keywords: IEnumRangeExceptions interface [Windows Sync],Next method, IEnumRangeExceptions.Next, IEnumRangeExceptions::Next, Next, Next method [Windows Sync], Next method [Windows Sync],IEnumRangeExceptions interface, winsync.ienumrangeexceptions_next, winsync/IEnumRangeExceptions::Next
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
 - IEnumRangeExceptions::Next
 - winsync/IEnumRangeExceptions::Next
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
 - IEnumRangeExceptions.Next
---

# IEnumRangeExceptions::Next


## -description

Returns the next elements in the change unit exception set, if they are available.

## -parameters

### -param cExceptions [in]

The number of range exception elements to retrieve in the range from zero to 1000.

### -param ppRangeException [out]

Returns the next <i>pcFetched</i> range exceptions.

### -param pcFetched [in, out]

Returns the number of range exceptions returned. This value can be <b>NULL</b> only if <i>cExceptions</i> is 1.

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
There are no more elements to retrieve.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ienumrangeexceptions">IEnumRangeExceptions Interface</a>
