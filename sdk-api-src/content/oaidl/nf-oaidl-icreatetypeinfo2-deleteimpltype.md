---
UID: NF:oaidl.ICreateTypeInfo2.DeleteImplType
title: ICreateTypeInfo2::DeleteImplType
author: windows-sdk-content
description: Deletes the IMPLTYPE flags for the indexed interface.
old-location: automat\icreatetypeinfo2_deleteimpltype.htm
old-project: automat
ms.assetid: c64b70eb-6047-4572-9d5e-f40b3c302f31
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: DeleteImplType, DeleteImplType method [Automation], DeleteImplType method [Automation],ICreateTypeInfo2 interface, ICreateTypeInfo2 interface [Automation],DeleteImplType method, ICreateTypeInfo2.DeleteImplType, ICreateTypeInfo2::DeleteImplType, _oa96_ICreateTypeInfo2_DeleteImplType, automat.icreatetypeinfo2_deleteimpltype, oaidl/ICreateTypeInfo2::DeleteImplType
ms.prod: windows
ms.technology: windows-sdk
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
-	ICreateTypeInfo2.DeleteImplType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ICreateTypeInfo2::DeleteImplType


## -description


Deletes the IMPLTYPE flags for the indexed interface.


## -parameters




### -param index [in]

The index of the interface for which to delete the type flags.



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
 




## -see-also




<a href="https://msdn.microsoft.com/34dc6f52-6864-4edb-b22d-80eef05d4c8c">ICreateTypeInfo2</a>
 

 

