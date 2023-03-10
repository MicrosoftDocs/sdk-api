---
UID: NF:winsync.IEnumSingleItemExceptions.Clone
title: IEnumSingleItemExceptions::Clone (winsync.h)
description: Clones the enumerator and returns a new enumerator that is in the same state as the current one. (IEnumSingleItemExceptions.Clone)
helpviewer_keywords: ["Clone","Clone method [Windows Sync]","Clone method [Windows Sync]","IEnumSingleItemExceptions interface","IEnumSingleItemExceptions interface [Windows Sync]","Clone method","IEnumSingleItemExceptions.Clone","IEnumSingleItemExceptions::Clone","winsync.ienumsingleitemexceptions_clone","winsync/IEnumSingleItemExceptions::Clone"]
old-location: winsync\ienumsingleitemexceptions_clone.htm
tech.root: winsync
ms.assetid: 89a02939-e761-450e-9479-29e19a872da6
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Sync], Clone method [Windows Sync],IEnumSingleItemExceptions interface, IEnumSingleItemExceptions interface [Windows Sync],Clone method, IEnumSingleItemExceptions.Clone, IEnumSingleItemExceptions::Clone, winsync.ienumsingleitemexceptions_clone, winsync/IEnumSingleItemExceptions::Clone
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
 - IEnumSingleItemExceptions::Clone
 - winsync/IEnumSingleItemExceptions::Clone
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
 - IEnumSingleItemExceptions.Clone
---

# IEnumSingleItemExceptions::Clone


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

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ienumsingleitemexceptions">IEnumSingleItemExceptions Interface</a>
