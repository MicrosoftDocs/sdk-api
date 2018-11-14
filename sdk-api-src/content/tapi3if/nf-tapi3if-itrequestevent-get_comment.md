---
UID: NF:tapi3if.ITRequestEvent.get_Comment
title: ITRequestEvent::get_Comment
author: windows-sdk-content
description: The get_Comment method gets the comment.
old-location: tapi3\itrequestevent_get_comment.htm
tech.root: tapi
ms.assetid: 2150d521-cbd2-457f-b3c6-97761941a442
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITRequestEvent interface [TAPI 2.2],get_Comment method, ITRequestEvent.get_Comment, ITRequestEvent::get_Comment, _tapi3_itrequestevent_get_comment, get_Comment, get_Comment method [TAPI 2.2], get_Comment method [TAPI 2.2],ITRequestEvent interface, tapi3.itrequestevent_get_comment, tapi3if/ITRequestEvent::get_Comment
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
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
 - ITRequestEvent.get_Comment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITRequestEvent.get_Comment
: 
---

# ITRequestEvent::get_Comment


## -description


The 
<b>get_Comment</b> method gets the comment.


## -parameters




### -param ppComment [out]

Pointer to a <b>BSTR</b> containing the comment.


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
The <i>ppComment</i> is not a valid pointer.

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
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>ppComment</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/69f9b504-be01-4167-8002-32a8e86bab0f">ITRequestEvent</a>
 

 

