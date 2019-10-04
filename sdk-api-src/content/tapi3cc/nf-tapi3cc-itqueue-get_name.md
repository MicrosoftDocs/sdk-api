---
UID: NF:tapi3cc.ITQueue.get_Name
title: ITQueue::get_Name (tapi3cc.h)
author: windows-sdk-content
description: The get_Name method gets the queue name.
old-location: tapi3\itqueue_get_name.htm
tech.root: Tapi
ms.assetid: c2a9f402-9341-426f-8994-902b754ceed9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITQueue interface [TAPI 2.2],get_Name method, ITQueue.get_Name, ITQueue::get_Name, _tapi3_itqueue_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITQueue interface, tapi3.itqueue_get_name, tapi3cc/ITQueue::get_Name
ms.topic: method
f1_keywords: 
 - "tapi3cc/ITQueue.get_Name"
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
 - ITQueue.get_Name
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITQueue::get_Name


## -description


The 
<b>get_Name</b> method gets the queue name.


## -parameters




### -param ppName [out]

Pointer to <b>BSTR</b> representation of queue name.


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
The <i>ppName</i> is not a valid pointer.

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



The application must use 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppName</i> parameter.
			




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueue">ITQueue</a>
 

 

