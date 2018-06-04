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

# ICreateTypeInfo::LayOut


## -description


Assigns VTBL offsets for virtual functions and instance offsets for per-instance data members, and creates the two type descriptions for dual interfaces.


## -parameters






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
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Cannot write to the destination.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_UNDEFINEDTYPE</b></dt>
</dl>
</td>
<td width="60%">
Bound to unrecognized type.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the type library is not valid for this operation.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_WRONGTYPEKIND</b></dt>
</dl>
</td>
<td width="60%">
Type mismatch.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The element cannot be found.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_AMBIGUOUSNAME</b></dt>
</dl>
</td>
<td width="60%">
More than one item exists with this name.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_SIZETOOBIG</b></dt>
</dl>
</td>
<td width="60%">
The type information is too long.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
Type mismatch.


</td>
</tr>
</table>
 




## -remarks



<b>LayOut</b> also assigns member ID numbers to the functions and variables, unless the TYPEKIND of the class is TKIND_DISPATCH. Call <b>LayOut</b> after all members of the type information are defined, and before the type library is saved.



Use <a href="https://msdn.microsoft.com/67824f38-e515-487e-8f4b-6682a5ac669c">ICreateTypeLib::SaveAllChanges</a> to save the type information after calling <b>LayOut</b>. Other members of the <a href="https://msdn.microsoft.com/c8bbb677-2666-4900-8fb9-788742eef656">ICreateTypeInfo</a> interface should not be called after calling <b>LayOut</b>.

<div class="alert"><b>Note</b>  Different implementations of <a href="https://msdn.microsoft.com/67824f38-e515-487e-8f4b-6682a5ac669c">ICreateTypeLib::SaveAllChanges</a> or other interfaces that create type information are free to assign any member ID numbers, provided that all members (including inherited members), have unique IDs. For examples, see <a href="https://msdn.microsoft.com/34dc6f52-6864-4edb-b22d-80eef05d4c8c">ICreateTypeInfo2</a>.
</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c8bbb677-2666-4900-8fb9-788742eef656">ICreateTypeInfo</a>
 

 

