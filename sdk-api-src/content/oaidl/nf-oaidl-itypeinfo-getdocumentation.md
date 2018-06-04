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

# ITypeInfo::GetDocumentation


## -description


Retrieves the documentation string, the complete Help file name and path, and the context ID for the Help topic for a specified type description.


## -parameters




### -param memid [in]

The ID of the member whose documentation is to be returned.




### -param pBstrName [out]

The name of the specified item. If the caller does not need the item name, <i>pBstrName</i> can be null.



### -param pBstrDocString [out]

The documentation string for the specified item. If the caller does not need the documentation string, <i>pBstrDocString</i> can be null.



### -param pdwHelpContext [out]

The Help localization context. If the caller does not need the Help context, it can be null.



### -param pBstrHelpFile [out]

The fully qualified name of the file containing the DLL used for Help file. If the caller does not need the file name, it can be null.


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



The function <b>GetDocumentation</b> provides access to the documentation for the member specified by the <i>memid</i> parameter. If the passed-in <i>memid</i> is MEMBERID_NIL, then the documentation for the type description is returned.



If the type description inherits from another type description, this function is recursive to the base type description, if necessary, to find the item with the requested member ID.



The caller should use <a href="https://msdn.microsoft.com/8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the BSTRs referenced by <i>pBstrName</i>, <i>pBstrDocString</i>, and <i>pBstrHelpFile</i>.





## -see-also




<a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>
 

 

