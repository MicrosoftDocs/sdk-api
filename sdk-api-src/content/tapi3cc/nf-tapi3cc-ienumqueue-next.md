---
UID: NF:tapi3cc.IEnumQueue.Next
title: IEnumQueue::Next
author: windows-sdk-content
description: The Next method gets the next specified number of elements in the enumeration sequence.
old-location: tapi3\ienumqueue_next.htm
old-project: Tapi
ms.assetid: 95c1a919-4138-49c1-ad3a-2b15d928e84f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IEnumQueue interface [TAPI 2.2],Next method, IEnumQueue.Next, IEnumQueue::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumQueue interface, _tapi3_ienumqueue_next, tapi3.ienumqueue_next, tapi3cc/IEnumQueue::Next
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AGENT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumQueue.Next
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumQueue::Next


## -description


The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence.


## -parameters




### -param celt [in]

Number of elements requested.


### -param ppElements [out]

Pointer to 
<a href="https://msdn.microsoft.com/dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023">ITQueue</a> list of interface pointers returned.


### -param pceltFetched [out]

Pointer to number of elements actually supplied. May be <b>NULL</b> if <i>celt</i> is one.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method returned <i>celt</i> number of elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements remaining was less than <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppElements</i> parameter is not a valid pointer.

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
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023">ITQueue</a> interface returned by <b>IEnumQueue::Next</b>. The application must call <b>Release</b> on the 
<b>ITQueue</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023">ITQueue</a>
 

 

