---
UID: NF:tapi3cc.IEnumQueue.Reset
title: IEnumQueue::Reset method
author: windows-driver-content
description: The Reset method resets the enumeration sequence to the beginning.
old-location: tapi3\ienumqueue_reset.htm
old-project: Tapi
ms.assetid: 0f444d56-e660-48c3-a483-256138d49984
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: IEnumQueue, IEnumQueue interface [TAPI 2.2], Reset method, IEnumQueue::Reset, Reset method [TAPI 2.2], Reset method [TAPI 2.2], IEnumQueue interface, Reset,IEnumQueue.Reset, _tapi3_ienumqueue_reset, tapi3.ienumqueue_reset, tapi3cc/IEnumQueue::Reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: AGENT_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	IEnumQueue.Reset
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumQueue::Reset method


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
 



