---
UID: NF:tapi3cc.IEnumQueue.Reset
title: IEnumQueue::Reset (tapi3cc.h)
description: The Reset method resets the enumeration sequence to the beginning.
helpviewer_keywords: ["IEnumQueue interface [TAPI 2.2]","Reset method","IEnumQueue.Reset","IEnumQueue::Reset","Reset","Reset method [TAPI 2.2]","Reset method [TAPI 2.2]","IEnumQueue interface","_tapi3_ienumqueue_reset","tapi3.ienumqueue_reset","tapi3cc/IEnumQueue::Reset"]
old-location: tapi3\ienumqueue_reset.htm
tech.root: tapi3
ms.assetid: 0f444d56-e660-48c3-a483-256138d49984
ms.date: 12/05/2018
ms.keywords: IEnumQueue interface [TAPI 2.2],Reset method, IEnumQueue.Reset, IEnumQueue::Reset, Reset, Reset method [TAPI 2.2], Reset method [TAPI 2.2],IEnumQueue interface, _tapi3_ienumqueue_reset, tapi3.ienumqueue_reset, tapi3cc/IEnumQueue::Reset
f1_keywords:
- tapi3cc/IEnumQueue.Reset
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- IEnumQueue.Reset
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumQueue::Reset


## -description


The 
<b>Reset</b> method resets the enumeration sequence to the beginning.


## -parameters






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
Method succeeded.

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
 



