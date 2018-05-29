---
UID: NF:oaidl.ITypeInfo2.GetVarIndexOfMemId
title: ITypeInfo2::GetVarIndexOfMemId
author: windows-sdk-content
description: Binds to a specific member based on a known DISPID, where the member name is not known (for example, when binding to a default member).
old-location: automat\itypeinfo2_getvarindexofmemid.htm
old-project: automat
ms.assetid: 6b97ddbf-bcb3-4e39-a355-40c1fd4e8c6a
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: GetVarIndexOfMemId, GetVarIndexOfMemId method [Automation], GetVarIndexOfMemId method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetVarIndexOfMemId method, ITypeInfo2.GetVarIndexOfMemId, ITypeInfo2::GetVarIndexOfMemId, _oa96_ITypeInfo2_GetVarIndexOfMemId, automat.itypeinfo2_getvarindexofmemid, oaidl/ITypeInfo2::GetVarIndexOfMemId
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
-	ITypeInfo2.GetVarIndexOfMemId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITypeInfo2::GetVarIndexOfMemId


## -description


Binds to a specific member based on a known DISPID, where the member name is not known (for example, when binding to a default member).


## -parameters




### -param memid [in]

The member identifier.


### -param pVarIndex [out]

The index.


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




<a href="https://msdn.microsoft.com/d3a34a13-6114-4f15-9de5-60da43fde600">ITypeInfo2</a>
 

 

