---
UID: NF:oaidl.ICreateTypeInfo2.DeleteVarDescByMemId
title: ICreateTypeInfo2::DeleteVarDescByMemId
author: windows-driver-content
description: Deletes the specified VARDESC structure.
old-location: automat\icreatetypeinfo2_deletevardescbymemid.htm
old-project: automat
ms.assetid: 5b69dda9-01b5-45b2-ab92-65a29a2d1f21
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: DeleteVarDescByMemId, DeleteVarDescByMemId method [Automation], DeleteVarDescByMemId method [Automation],ICreateTypeInfo2 interface, ICreateTypeInfo2 interface [Automation],DeleteVarDescByMemId method, ICreateTypeInfo2.DeleteVarDescByMemId, ICreateTypeInfo2::DeleteVarDescByMemId, _oa96_ICreateTypeInfo2_DeleteVarDescByMemId, automat.icreatetypeinfo2_deletevardescbymemid, oaidl/ICreateTypeInfo2::DeleteVarDescByMemId
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
-	ICreateTypeInfo2.DeleteVarDescByMemId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ICreateTypeInfo2::DeleteVarDescByMemId


## -description


Deletes the specified VARDESC structure.


## -parameters




### -param memid [in]

The member identifier of the VARDESC to be deleted.



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
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_IOERROR</b></dt>
</dl>
</td>
<td width="60%">
The function cannot read from the file.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVDATAREAD</b></dt>
</dl>
</td>
<td width="60%">
The function cannot read from the file.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_UNSUPFORMAT</b></dt>
</dl>
</td>
<td width="60%">
The type library has an old format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The type library cannot be opened.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/34dc6f52-6864-4edb-b22d-80eef05d4c8c">ICreateTypeInfo2</a>
 

 

