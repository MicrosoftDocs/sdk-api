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

# ITypeInfo::GetIDsOfNames


## -description


Maps between member names and member IDs, and parameter names and parameter IDs.


## -parameters




### -param rgszNames [in]

An array of names to be mapped.




### -param cNames [in]

The count of the names to be mapped.


### -param pMemId [out]

Caller-allocated array in which name mappings are placed.


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



The function <a href="https://msdn.microsoft.com/6f6cf233-3481-436e-8d6a-51f93bf91619">GetIDsOfNames</a> maps the name of a member (<b>rgszNames</b>[0]) and its parameters (<b>rgszNames</b>[1] ...<b>rgszNames</b>[<b>cNames</b>- 1]) to the ID of the member (<b>pMemId</b>[0]), and to the IDs of the specified parameters (<b>pMemId</b>[1] ... <b>pMemId</b>[<b>cNames</b>- 1]). The IDs of parameters are 0 for the first parameter in the member function's argument list, 1 for the second, and so on.



If the type description inherits from another type description, this function is recursive to the base type description, if necessary, to find the item with the requested member ID.





## -see-also




<a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>
 

 

