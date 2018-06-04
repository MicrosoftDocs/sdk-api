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

# ITypeInfo::GetNames


## -description


Retrieves the variable with the specified member ID or the name of the property or method and the parameters that correspond to the specified function ID.


## -parameters




### -param memid [in]

The ID of the member whose name (or names) is to be returned.




### -param rgBstrNames [out]

The caller-allocated array. On return, each of the elements contains the name (or names) associated with the member.


### -param cMaxNames [in]

The length of the passed-in <i>rgBstrNames</i> array.


### -param pcNames [out]

The number of names in the <i>rgBstrNames</i> array.


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
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



The caller must release the returned BSTR array.



If the member ID identifies a property that is implemented with property functions, the property name is returned. For property get functions, the names of the function and its parameters are always returned.



For property put and put reference functions, the right side of the assignment is unnamed. If <i>cMaxNames</i> is less than is required to return all of the names of the parameters of a function, then only the names of the first <i>cMaxNames</i> - 1 parameters are returned. The names of the parameters are returned in the array in the same order that they appear elsewhere in the interface (for example, the same order in the parameter array associated with the FUNCDESC enumeration).



If the type description inherits from another type description, this function is recursive to the base type description, if necessary, to find the item with the requested member ID.





## -see-also




<a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>
 

 

