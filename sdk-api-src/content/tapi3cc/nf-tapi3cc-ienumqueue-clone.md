---
UID: NF:tapi3cc.IEnumQueue.Clone
title: IEnumQueue::Clone
author: windows-sdk-content
description: The Clone method creates another enumerator that contains the same enumeration state as the current one.
old-location: tapi3\ienumqueue_clone.htm
tech.root: tapi
ms.assetid: e63df5aa-8c90-4978-a63f-96ac5f624ef4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumQueue interface, IEnumQueue interface [TAPI 2.2],Clone method, IEnumQueue.Clone, IEnumQueue::Clone, _tapi3_ienumqueue_clone, tapi3.ienumqueue_clone, tapi3cc/IEnumQueue::Clone
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
 - IEnumQueue.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumQueue::Clone


## -description


The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one.


## -parameters




### -param ppEnum [out]

Pointer to new 
<a href="https://msdn.microsoft.com/0bbe3533-d5ce-447b-82e1-3bd61c5a7ca2">IEnumQueue</a> interface.


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
The <i>ppEnum</i> parameter is not a valid pointer.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Failed for unknown reasons.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/0bbe3533-d5ce-447b-82e1-3bd61c5a7ca2">IEnumQueue</a> interface returned by <b>IEnumQueue::Clone</b>. The application must call <b>Release</b> on the 
<b>IEnumQueue</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/0bbe3533-d5ce-447b-82e1-3bd61c5a7ca2">IEnumQueue</a>
 

 

