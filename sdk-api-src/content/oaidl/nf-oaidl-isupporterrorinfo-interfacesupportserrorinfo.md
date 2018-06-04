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

# ISupportErrorInfo::InterfaceSupportsErrorInfo


## -description


Indicates whether an interface supports the <a href="https://msdn.microsoft.com/4dda6909-2d9a-4727-ae0c-b5f90dcfa447">IErrorInfo</a> interface.


## -parameters




### -param riid [in]

An interface identifier (IID).


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
The interface supports <a href="https://msdn.microsoft.com/4dda6909-2d9a-4727-ae0c-b5f90dcfa447">IErrorInfo</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The interface does not support <a href="https://msdn.microsoft.com/4dda6909-2d9a-4727-ae0c-b5f90dcfa447">IErrorInfo</a>.

</td>
</tr>
</table>
 




## -remarks



Objects that support the <a href="https://msdn.microsoft.com/4dda6909-2d9a-4727-ae0c-b5f90dcfa447">IErrorInfo</a> interface must also implement this interface.



Programs that receive an error return value should call <b>QueryInterface</b> to get a pointer to the <a href="https://msdn.microsoft.com/42d33066-36b4-4a5b-aa5d-46682e560f32">ISupportErrorInfo</a>

interface, and then call <b>InterfaceSupportsErrorInfo</b> with the <i>riid</i> of the interface that returned the return value. If <b>InterfaceSupportsErrorInfo</b> returns S_FALSE, then the error object does not represent an error returned from the caller, but from somewhere else. In this case, the error object can be considered incorrect and should be discarded.



If <a href="https://msdn.microsoft.com/42d33066-36b4-4a5b-aa5d-46682e560f32">ISupportErrorInfo</a> returns S_OK, use the <a href="https://msdn.microsoft.com/03317526-8c4f-4173-bc10-110c8112676a">GetErrorInfo</a> function to get a pointer to the error object.



For an example that demonstrates implementing <b>InterfaceSupportsErrorInfo</b>, see the ErrorInfo.cpp file in the COM Fundamentals Lines sample.




## -see-also




<a href="https://msdn.microsoft.com/42d33066-36b4-4a5b-aa5d-46682e560f32">ISupportErrorInfo</a>
 

 

