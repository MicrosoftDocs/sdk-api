---
UID: NF:winsync.IEnumRangeExceptions.Skip
title: IEnumRangeExceptions::Skip (winsync.h)
description: Skips the specified number of range exceptions.
helpviewer_keywords: ["IEnumRangeExceptions interface [Windows Sync]","Skip method","IEnumRangeExceptions.Skip","IEnumRangeExceptions::Skip","Skip","Skip method [Windows Sync]","Skip method [Windows Sync]","IEnumRangeExceptions interface","winsync.ienumrangeexceptions_skip","winsync/IEnumRangeExceptions::Skip"]
old-location: winsync\ienumrangeexceptions_skip.htm
tech.root: winsync
ms.assetid: 61907858-4089-4c12-865c-623a43132be3
ms.date: 12/05/2018
ms.keywords: IEnumRangeExceptions interface [Windows Sync],Skip method, IEnumRangeExceptions.Skip, IEnumRangeExceptions::Skip, Skip, Skip method [Windows Sync], Skip method [Windows Sync],IEnumRangeExceptions interface, winsync.ienumrangeexceptions_skip, winsync/IEnumRangeExceptions::Skip
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
 - IEnumRangeExceptions::Skip
 - winsync/IEnumRangeExceptions::Skip
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
 - IEnumRangeExceptions.Skip
---

# IEnumRangeExceptions::Skip


## -description

Skips the specified number of range exceptions.

## -parameters

### -param cExceptions [in]

The number of range exceptions to skip.

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
The enumerator reaches the end of the list before it can skip <i>cExceptions</i> range exceptions. In this case, the enumerator skips as many elements as possible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARGS</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ienumrangeexceptions">IEnumRangeExceptions Interface</a>