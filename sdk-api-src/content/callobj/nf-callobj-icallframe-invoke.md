---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ICallFrame::Invoke


## -description


Applies this activation record to an object.
In a marshalling situation, typically this is carried out on the server side, and is the means by which the work of the actual object is accomplished.


## -parameters




### -param pvReceiver [in]

The interface on which the invocation is to occur. The caller is responsible for ensuring that this interface is of the appropriate IID; the implementation will simply do a cast and assume that is the case.


### -param param






## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CALLFRAME_E_ALREADYINVOKED</b></dt>
</dl>
</td>
<td width="60%">
An invocation has already been made from this frame.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>
 




## -remarks



Generally speaking, carrying out the invocation involves allocating a new stack frame, shallow-copying down the data in the original frame, then calling the appropriate method in the indicated object. The object invoked may then choose to modify [out] parameters, which are reachable from the copied frame, according to the appropriate semantics of the invocation. When the invocation returns from the object, the call frame automatically captures the return value from <a href="https://msdn.microsoft.com/848cccc7-19c8-4ce6-b609-bcf798ec8c76">ICallFrame::SetReturnValue</a>.




## -see-also




<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>
 

 

