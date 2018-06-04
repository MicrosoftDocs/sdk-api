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

# OleSetContainedObject function


## -description


Notifies an object that it is embedded in an OLE container, which ensures that reference counting is done correctly for containers that support links to embedded objects.




## -parameters




### -param pUnknown [in]

Pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the object.


### -param fContained [in]

<b>TRUE</b> if the object is an embedded object; <b>FALSE</b> otherwise.


## -returns



This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
</table>
 




## -remarks



The <b>OleSetContainedObject</b> function notifies an object that it is embedded in an OLE container. The implementation of <b>OleSetContainedObject</b> was changed in OLE 2.01 to coincide with the publication of the <a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a> interface. You can use <b>OleSetContainedObject</b> and the <a href="https://msdn.microsoft.com/dbd3f632-2b81-44d1-8376-4b507316895f">IRunnableObject::SetContainedObject</a> method interchangeably. The <b>OleSetContainedObject</b> function queries the object for a pointer to the <b>IRunnableObject</b> interface. If successful, the function returns the results of calling <b>IRunnableObject::SetContainedObject</b>.






## -see-also




<a href="https://msdn.microsoft.com/dbd3f632-2b81-44d1-8376-4b507316895f">IRunnableObject::SetContainedObject</a>
 

 

