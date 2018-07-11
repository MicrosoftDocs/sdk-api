---
UID: NF:oaidl.ITypeInfo.GetRefTypeOfImplType
title: ITypeInfo::GetRefTypeOfImplType
author: windows-sdk-content
description: If a type description describes a COM class, it retrieves the type description of the implemented interface types.
old-location: automat\itypeinfo_getreftypeofimpltype.htm
old-project: automat
ms.assetid: aec61a9a-fa4f-42cd-a74b-100cdf2c2624
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: GetRefTypeOfImplType, GetRefTypeOfImplType method [Automation], GetRefTypeOfImplType method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetRefTypeOfImplType method, ITypeInfo.GetRefTypeOfImplType, ITypeInfo::GetRefTypeOfImplType, _oa96_ITypeInfo_GetRefTypeOfImplType, automat.itypeinfo_getreftypeofimpltype, oaidl/ITypeInfo::GetRefTypeOfImplType
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
tech.root: 
req.typenames: VARKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ITypeInfo.GetRefTypeOfImplType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITypeInfo::GetRefTypeOfImplType


## -description


If a type description describes a COM class, it retrieves the type description of the implemented interface types. For an interface, <b>GetRefTypeOfImplType</b> returns the type information for inherited interfaces, if any exist.


## -parameters




### -param index [in]

The index of the implemented type whose handle is returned. The valid range is 0 to the <b>cImplTypes</b> field in the TYPEATTR structure.




### -param pRefType [out]

A handle for the implemented interface (if any). This handle can be passed to <a href="https://msdn.microsoft.com/61d3b31d-6591-4e55-9e82-5246a168be00">ITypeInfo::GetRefTypeInfo</a> to get the type description.


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
<dt><b>TYPE_E_ELEMENTNOTFOUND
</b></dt>
</dl>
</td>
<td width="60%">
Passed index is outside the range 0 to 1 less than the number of function descriptions.

</td>
</tr>
</table>
 




## -remarks



If the TKIND_DISPATCH type description is for a dual interface, the TKIND_INTERFACE type description can be obtained by calling <b>GetRefTypeOfImplType</b> with an <i>indexof</i> –1, and by passing the returned <i>pRefTypehandle</i> to <a href="https://msdn.microsoft.com/61d3b31d-6591-4e55-9e82-5246a168be00">GetRefTypeInfo</a> to retrieve the type information.





## -see-also




<a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>
 

 

