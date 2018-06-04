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

# OleRun function


## -description


Puts an OLE compound document object into the running state.


## -parameters




### -param pUnknown [in]

Pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the object, with which it will query for a pointer to the <a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a> interface, and then call its <a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">Run</a> method.


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
<dt><b>OLE_E_CLASSDIFF</b></dt>
</dl>
</td>
<td width="60%">
The source of an OLE link has been converted to a different class.

</td>
</tr>
</table>
 




## -remarks



The <b>OleRun</b> function puts an object in the running state. The implementation of <b>OleRun</b> was changed in OLE 2.01 to coincide with the publication of the <a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a> interface. You can use <b>OleRun</b> and <a href="https://msdn.microsoft.com/fb79e81c-0655-48ea-afb5-dab3529676d0">IRunnableObject::Run</a> interchangeably. <b>OleRun</b> queries the object for a pointer to <b>IRunnableObject</b>. If successful, the function returns the results of calling the <b>IRunnableObject::Run</b> method.

For more information on using this function, see <a href="https://msdn.microsoft.com/fb79e81c-0655-48ea-afb5-dab3529676d0">IRunnableObject::Run</a>.




## -see-also




<a href="https://msdn.microsoft.com/1fadd27d-cb2c-47fc-891a-16f82bdac0f6">IOleLink::BindToSource</a>



<a href="https://msdn.microsoft.com/fb79e81c-0655-48ea-afb5-dab3529676d0">IRunnableObject::Run</a>
 

 

