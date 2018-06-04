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

# SetContextPropertyValue function


## -description



Adds a property to the recognizer context.

If a property already exists, its value is modified.




## -parameters




### -param hrc

The handle to the recognizer context.


### -param pGuid

TBD


### -param cbSize

The size, in bytes, of the <i>pProperty</i> buffer.


### -param pProperty

The buffer that contains the property value.


#### - pGUID

The property to set. Specify a predefined property globally unique identifier (GUID) or application-defined property GUID. For a list of predefined properties, see the recognition <a href="https://msdn.microsoft.com/dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e">Property GUIDs</a>.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pGUID</i> is invalid or <i>cbSize</i> has been set to a very large, invalid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_INVALID_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
<i>pGUID</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>cbSize</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Returned when an attempt is made to set a property value when it has already been enabled.

</td>
</tr>
</table>
 




## -remarks



The <b>SetContextPropertyValue</b> function is optional.




## -see-also




<a href="https://msdn.microsoft.com/3d3df56f-d989-4d3b-a0e2-00a7ac0fabd6">GetContextPropertyList Function</a>



<a href="https://msdn.microsoft.com/e3f154ce-b4bf-4520-a4de-03cfe27ef9b0">GetContextPropertyValue Function</a>
 

 

