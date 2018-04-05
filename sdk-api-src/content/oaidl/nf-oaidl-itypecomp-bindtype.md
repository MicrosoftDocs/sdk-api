---
UID: NF:oaidl.ITypeComp.BindType
title: ITypeComp::BindType method
author: windows-driver-content
description: Binds to the type descriptions contained within a type library.
old-location: automat\itypecomp_bindtype.htm
old-project: automat
ms.assetid: e1b6eb9c-aa5a-41b9-bc97-afa82206ccef
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: BindType method [Automation], BindType method [Automation], ITypeComp interface, BindType,ITypeComp.BindType, ITypeComp, ITypeComp interface [Automation], BindType method, ITypeComp::BindType, _oa96_ITypeComp_BindType, automat.itypecomp_bindtype, oaidl/ITypeComp::BindType
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
-	ITypeComp.BindType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ITypeComp::BindType method


## -description


Binds to the type descriptions contained within a type library.


## -parameters




### -param szName [in]

The name to be bound.


### -param lHashVal [in]

The hash value for the name computed by <a href="https://msdn.microsoft.com/7cd401dc-95d0-4628-88f9-d00969228ea8">LHashValOfName</a>.


### -param ppTInfo [out]

 An <a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a> of the type to which the name was bound.



### -param ppTComp [out]

Passes a valid pointer, such as the address of an <a href="https://msdn.microsoft.com/4d35370f-506f-45cd-9d75-e48c640d8f4d">ITypeComp</a> variable.


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



Use the function <b>BindType</b> for binding a type name to the <a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a> that describes the type. This function is invoked on the <a href="https://msdn.microsoft.com/4d35370f-506f-45cd-9d75-e48c640d8f4d">ITypeComp</a> that is returned by <a href="https://msdn.microsoft.com/11c22e52-b0d5-4251-b8fa-ea3efae555e6">ITypeLib::GetTypeComp</a> to bind to types defined within that library. It can also be used in the future for binding to nested types.





## -see-also




<a href="https://msdn.microsoft.com/4d35370f-506f-45cd-9d75-e48c640d8f4d">ITypeComp</a>
 

 

