---
UID: NF:tapi3.ITQueue.get_CurrentCallsQueued
title: ITQueue::get_CurrentCallsQueued (tapi3.h)
description: The ITQueue::get_CurrentCallsQueued (tapi3.h) method gets the number of incoming calls currently waiting.
helpviewer_keywords: ["ITQueue interface [TAPI 2.2]","get_CurrentCallsQueued method","ITQueue.get_CurrentCallsQueued","ITQueue::get_CurrentCallsQueued","_tapi3_itqueue_get_currentcallsqueued","get_CurrentCallsQueued","get_CurrentCallsQueued method [TAPI 2.2]","get_CurrentCallsQueued method [TAPI 2.2]","ITQueue interface","tapi3.itqueue_get_currentcallsqueued","tapi3cc/ITQueue::get_CurrentCallsQueued"]
old-location: tapi3\itqueue_get_currentcallsqueued.htm
tech.root: tapi3
ms.assetid: cbc6e38c-c4e9-45ea-8c9a-9bb8116c1e2f
ms.date: 08/10/2022
ms.keywords: ITQueue interface [TAPI 2.2],get_CurrentCallsQueued method, ITQueue.get_CurrentCallsQueued, ITQueue::get_CurrentCallsQueued, _tapi3_itqueue_get_currentcallsqueued, get_CurrentCallsQueued, get_CurrentCallsQueued method [TAPI 2.2], get_CurrentCallsQueued method [TAPI 2.2],ITQueue interface, tapi3.itqueue_get_currentcallsqueued, tapi3cc/ITQueue::get_CurrentCallsQueued
req.header: tapi3.h
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
 - ITQueue::get_CurrentCallsQueued
 - tapi3/ITQueue::get_CurrentCallsQueued
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
 - ITQueue.get_CurrentCallsQueued
---

# ITQueue::get_CurrentCallsQueued


## -description

The 
<b>get_CurrentCallsQueued</b> method gets the number of incoming calls currently waiting.

## -parameters

### -param plCalls [out]

Pointer to the number of incoming calls in the queue.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plCalls</i> is not a valid pointer.

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

## -see-also

<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueue">ITQueue</a>
