---
UID: NF:oaidl.ICreateTypeInfo.LayOut
title: ICreateTypeInfo::LayOut
author: windows-driver-content
description: Assigns VTBL offsets for virtual functions and instance offsets for per-instance data members, and creates the two type descriptions for dual interfaces.
old-location: automat\icreatetypeinfo_layout.htm
old-project: automat
ms.assetid: 3880aad3-8a6f-43e6-8420-25c4d1b9a71a
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: ICreateTypeInfo interface [Automation],LayOut method, ICreateTypeInfo.LayOut, ICreateTypeInfo::LayOut, LayOut, LayOut method [Automation], LayOut method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_LayOut, automat.icreatetypeinfo_layout, oaidl/ICreateTypeInfo::LayOut
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VARKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	oaidl.h
api_name:
-	ICreateTypeInfo.LayOut
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

