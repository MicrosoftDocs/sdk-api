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

# ITypeInfo::GetRefTypeOfImplType


## -description


If a type description describes a COM class, it retrieves the type description of the implemented interface types. For an interface, <b>GetRefTypeOfImplType</b> returns the type information for inherited interfaces, if any exist.


## -parameters




### -param index [in]

The index of the implemented type whose handle is returned. The valid range is 0 to the <b>cImplTypes</b> field in the TYPEATTR structure.




### -param pRefType [out]

A handle for the implemented interface (if any). This handle can be passed to <a href="https://msdn.microsoft.com/61d3b31d-6591-4e55-9e82-5246a168be00">ITypeInfo::GetRefTypeInfo</a> to get the type description.


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
<dt><b>TYPE_E_ELEMENTNOTFOUND
</b></dt>
</dl>
</td>
<td width="60%">
Passed index is outside the range 0 to 1 less than the number of function descriptions.

</td>
</tr>
</table>
 




## -remarks



If the TKIND_DISPATCH type description is for a dual interface, the TKIND_INTERFACE type description can be obtained by calling <b>GetRefTypeOfImplType</b> with an <i>indexof</i> –1, and by passing the returned <i>pRefTypehandle</i> to <a href="https://msdn.microsoft.com/61d3b31d-6591-4e55-9e82-5246a168be00">GetRefTypeInfo</a> to retrieve the type information.





## -see-also




<a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>
 

 

