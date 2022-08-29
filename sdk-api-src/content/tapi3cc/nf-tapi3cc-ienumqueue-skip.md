---
UID: NF:tapi3cc.IEnumQueue.Skip
title: IEnumQueue::Skip (tapi3cc.h)
description: The IEnumQueue::Skip method (tapi3cc.h) skips over the next specified number of elements in the enumeration sequence.
helpviewer_keywords: ["IEnumQueue interface [TAPI 2.2]","Skip method","IEnumQueue.Skip","IEnumQueue::Skip","Skip","Skip method [TAPI 2.2]","Skip method [TAPI 2.2]","IEnumQueue interface","_tapi3_ienumqueue_skip","tapi3.ienumqueue_skip","tapi3cc/IEnumQueue::Skip"]
old-location: tapi3\ienumqueue_skip.htm
tech.root: tapi3
ms.assetid: 92862b33-ceaf-4b18-b782-bb0352871d34
ms.date: 08/09/2022
ms.keywords: IEnumQueue interface [TAPI 2.2],Skip method, IEnumQueue.Skip, IEnumQueue::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumQueue interface, _tapi3_ienumqueue_skip, tapi3.ienumqueue_skip, tapi3cc/IEnumQueue::Skip
req.header: tapi3cc.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumQueue::Skip
 - tapi3cc/IEnumQueue::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumQueue.Skip
---

# IEnumQueue::Skip


## -description

The 
<b>Skip</b> method skips over the next specified number of elements in the enumeration sequence.

## -parameters

### -param celt [in]

Number of elements to skip.

## -returns

This method can return one of these values.

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
Number of elements skipped was <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements skipped was not <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

