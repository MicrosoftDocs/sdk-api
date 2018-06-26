---
UID: NF:oaidl.ITypeInfo.GetTypeComp
title: ITypeInfo::GetTypeComp
author: windows-sdk-content
description: Retrieves the ITypeComp interface for the type description, which enables a client compiler to bind to the type description's members.
old-location: automat\itypeinfo_gettypecomp.htm
old-project: automat
ms.assetid: 094cf9d5-2d9b-4c3c-844e-45737e905099
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: GetTypeComp, GetTypeComp method [Automation], GetTypeComp method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetTypeComp method, ITypeInfo.GetTypeComp, ITypeInfo::GetTypeComp, _oa96_ITypeInfo_GetTypeComp, automat.itypeinfo_gettypecomp, oaidl/ITypeInfo::GetTypeComp
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
 - ITypeInfo.GetTypeComp
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITypeInfo::GetTypeComp


## -description


Retrieves the <a href="https://msdn.microsoft.com/4d35370f-506f-45cd-9d75-e48c640d8f4d">ITypeComp</a> interface for the type description, which enables a client compiler to bind to the type description's members.


## -parameters




### -param ppTComp [out]

The <a href="https://msdn.microsoft.com/4d35370f-506f-45cd-9d75-e48c640d8f4d">ITypeComp</a> of the containing type library.


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



A client compiler can use the <a href="https://msdn.microsoft.com/4d35370f-506f-45cd-9d75-e48c640d8f4d">ITypeComp</a> interface to bind to members of the type.





## -see-also




<a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>
 

 

