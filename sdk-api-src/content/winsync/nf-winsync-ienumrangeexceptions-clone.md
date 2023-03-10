---
UID: NF:winsync.IEnumRangeExceptions.Clone
title: IEnumRangeExceptions::Clone (winsync.h)
description: Clones the enumerator and returns a new enumerator that is in the same state as the current one. (IEnumRangeExceptions.Clone)
helpviewer_keywords: ["Clone","Clone method [Windows Sync]","Clone method [Windows Sync]","IEnumRangeExceptions interface","IEnumRangeExceptions interface [Windows Sync]","Clone method","IEnumRangeExceptions.Clone","IEnumRangeExceptions::Clone","winsync.ienumrangeexceptions_clone","winsync/IEnumRangeExceptions::Clone"]
old-location: winsync\ienumrangeexceptions_clone.htm
tech.root: winsync
ms.assetid: b9ba5d49-754f-4eb0-972b-67e9a6a41994
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Sync], Clone method [Windows Sync],IEnumRangeExceptions interface, IEnumRangeExceptions interface [Windows Sync],Clone method, IEnumRangeExceptions.Clone, IEnumRangeExceptions::Clone, winsync.ienumrangeexceptions_clone, winsync/IEnumRangeExceptions::Clone
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
 - IEnumRangeExceptions::Clone
 - winsync/IEnumRangeExceptions::Clone
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
 - IEnumRangeExceptions.Clone
---

# IEnumRangeExceptions::Clone


## -description

Clones the enumerator and returns a new enumerator that is in the same state as the current one.

## -parameters

### -param ppEnum [out]

Returns the newly cloned enumerator.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ienumrangeexceptions">IEnumRangeExceptions Interface</a>
