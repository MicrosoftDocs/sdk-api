---
UID: NF:winsync.IEnumChangeUnitExceptions.Next
title: IEnumChangeUnitExceptions::Next (winsync.h)
description: Returns the next elements in the change unit exception set, if they are available. (IEnumChangeUnitExceptions.Next)
helpviewer_keywords: ["IEnumChangeUnitExceptions interface [Windows Sync]","Next method","IEnumChangeUnitExceptions.Next","IEnumChangeUnitExceptions::Next","Next","Next method [Windows Sync]","Next method [Windows Sync]","IEnumChangeUnitExceptions interface","winsync.ienumchangeunitexceptions_next","winsync/IEnumChangeUnitExceptions::Next"]
old-location: winsync\ienumchangeunitexceptions_next.htm
tech.root: winsync
ms.assetid: 97bf473d-4e63-4192-a5d8-b802d5887a55
ms.date: 12/05/2018
ms.keywords: IEnumChangeUnitExceptions interface [Windows Sync],Next method, IEnumChangeUnitExceptions.Next, IEnumChangeUnitExceptions::Next, Next, Next method [Windows Sync], Next method [Windows Sync],IEnumChangeUnitExceptions interface, winsync.ienumchangeunitexceptions_next, winsync/IEnumChangeUnitExceptions::Next
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
 - IEnumChangeUnitExceptions::Next
 - winsync/IEnumChangeUnitExceptions::Next
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
 - IEnumChangeUnitExceptions.Next
---

# IEnumChangeUnitExceptions::Next


## -description

Returns the next elements in the change unit exception set, if they are available.

## -parameters

### -param cExceptions [in]

The number of change unit exceptions to retrieve in the range of zero to 1000.

### -param ppChangeUnitException [out]

Returns the next <i>pcFetched</i> change unit exceptions.

### -param pcFetched [in, out]

Returns the number of change unit exceptions that are retrieved. This value can be <b>NULL</b> only if <i>cExceptions</i> is 1.

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
If there are no more change unit exceptions to retrieve.

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

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ienumchangeunitexceptions">IEnumChangeUnitExceptions Interface</a>
