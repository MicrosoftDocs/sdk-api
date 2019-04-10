---
UID: NF:oaidl.ICreateTypeInfo.AddImplType
title: ICreateTypeInfo::AddImplType (oaidl.h)
author: windows-sdk-content
description: Specifies an inherited interface, or an interface implemented by a component object class (coclass).
old-location: automat\icreatetypeinfo_addimpltype.htm
tech.root: automat
ms.assetid: fef8421f-67de-402b-8efd-7a104c84ca6e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddImplType, AddImplType method [Automation], AddImplType method [Automation],ICreateTypeInfo interface, ICreateTypeInfo interface [Automation],AddImplType method, ICreateTypeInfo.AddImplType, ICreateTypeInfo::AddImplType, _oa96_ICreateTypeInfo_AddImplType, automat.icreatetypeinfo_addimpltype, oaidl/ICreateTypeInfo::AddImplType
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ICreateTypeInfo.AddImplType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreateTypeInfo::AddImplType


## -description


Specifies an inherited interface, or an interface implemented by a component object class (coclass).


## -parameters




### -param index [in]

The index of the implementation class to be added. Specifies the order of the type relative to the other type.




### -param hRefType [in]

A handle to the referenced type description obtained from the <a href="https://msdn.microsoft.com/cb7f41f1-81a6-406f-916f-d1d1a8c093b5">AddRefType</a> description.



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
<dt><b>TYPE_E_WRONGTYPEKIND</b></dt>
</dl>
</td>
<td width="60%">
Type mismatch.

</td>
</tr>
</table>
 




## -remarks



To specify an inherited interface, use index = 0. For a dispinterface with Syntax 2, call <b>ICreateTypeInfo::AddImplType</b> twice, once with <i>index</i> = 0 for the inherited <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> and once with <i>index</i> = 1 for the interface that is being wrapped. For a dual interface, call <b>ICreateTypeInfo::AddImplType</b> with <i>index</i> = -1 for the TKIND_INTERFACE type information component of the dual interface.





## -see-also




<a href="https://msdn.microsoft.com/c8bbb677-2666-4900-8fb9-788742eef656">ICreateTypeInfo</a>
 

 

