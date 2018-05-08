---
UID: NF:oaidl.ICreateTypeInfo2.DeleteFuncDescByMemId
title: ICreateTypeInfo2::DeleteFuncDescByMemId
author: windows-driver-content
description: Deletes the specified function description (FUNCDESC).
old-location: automat\icreatetypeinfo2_deletefuncdescbymemid.htm
old-project: automat
ms.assetid: 75de562b-3c08-4bab-957a-3a9eab16fb3f
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: DeleteFuncDescByMemId, DeleteFuncDescByMemId method [Automation], DeleteFuncDescByMemId method [Automation],ICreateTypeInfo2 interface, ICreateTypeInfo2 interface [Automation],DeleteFuncDescByMemId method, ICreateTypeInfo2.DeleteFuncDescByMemId, ICreateTypeInfo2::DeleteFuncDescByMemId, _oa96_ICreateTypeInfo2_DeleteFuncDescByMemId, automat.icreatetypeinfo2_deletefuncdescbymemid, oaidl/ICreateTypeInfo2::DeleteFuncDescByMemId
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
-	ICreateTypeInfo2.DeleteFuncDescByMemId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ICreateTypeInfo2::DeleteFuncDescByMemId


## -description


Deletes the specified function description (FUNCDESC).


## -parameters




### -param memid [in]

The member identifier of the FUNCDESC to delete.




### -param invKind [in]

The type of the invocation.


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
 

 

