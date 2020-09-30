---
UID: NF:winsync.IEnumChangeUnitExceptions.Skip
title: IEnumChangeUnitExceptions::Skip (winsync.h)
description: Skips the specified number of change unit exceptions.
helpviewer_keywords: ["IEnumChangeUnitExceptions interface [Windows Sync]","Skip method","IEnumChangeUnitExceptions.Skip","IEnumChangeUnitExceptions::Skip","Skip","Skip method [Windows Sync]","Skip method [Windows Sync]","IEnumChangeUnitExceptions interface","winsync.ienumchangeunitexceptions_skip","winsync/IEnumChangeUnitExceptions::Skip"]
old-location: winsync\ienumchangeunitexceptions_skip.htm
tech.root: winsync
ms.assetid: 71e325cc-b686-4db5-988f-abf08af48d1c
ms.date: 12/05/2018
ms.keywords: IEnumChangeUnitExceptions interface [Windows Sync],Skip method, IEnumChangeUnitExceptions.Skip, IEnumChangeUnitExceptions::Skip, Skip, Skip method [Windows Sync], Skip method [Windows Sync],IEnumChangeUnitExceptions interface, winsync.ienumchangeunitexceptions_skip, winsync/IEnumChangeUnitExceptions::Skip
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
 - IEnumChangeUnitExceptions::Skip
 - winsync/IEnumChangeUnitExceptions::Skip
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
 - IEnumChangeUnitExceptions.Skip
---

# IEnumChangeUnitExceptions::Skip


## -description

Skips the specified number of change unit exceptions.

## -parameters

### -param cExceptions [in]

The number of change unit exceptions to skip.

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
The enumerator reaches the end of the list before it can skip the specified number of change unit exceptions. In this case, the enumerator skips as many elements as possible.

</td>
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