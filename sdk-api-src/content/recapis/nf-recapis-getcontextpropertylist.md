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

# GetContextPropertyList function


## -description



Retrieves a list of properties the recognizer supports.




## -parameters




### -param hrc

The handle to the recognizer context.


### -param pcProperties

On input, the size, in bytes, the <i>pPropertyGUIDS</i> buffer can be. On output, the size, in bytes, the <i>pPropertyGUIDS</i> buffer is.


### -param pPropertyGUIDS

The user-allocated buffer to contain a list of properties the recognizer supports. To determine the size of the buffer, set <i>pPropertyGUIDS</i> to <b>NULL</b>; use the size (<i>pcProperties</i>) to allocate <i>pPropertyGUIDS</i>. For a list of predefined properties, see the recognition <a href="https://msdn.microsoft.com/dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e">Property GUIDs</a>.


## -returns



This function can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppPropertyGUIDS</i> buffer is too small.

</td>
</tr>
</table>
 




## -remarks



This function is optional.

When Microsoft recognition engines are called with the <i>pcProperties</i> parameter set to a value larger than the required value, it does not result in an error. Instead, the engine automatically changes the size to the required value for the recognizer.




## -see-also




<a href="https://msdn.microsoft.com/e3f154ce-b4bf-4520-a4de-03cfe27ef9b0">GetContextPropertyValue Function</a>



<a href="https://msdn.microsoft.com/42b1857d-92ee-456f-aafc-b8780526a137">SetContextPropertyValue Function</a>
 

 

