---
UID: NF:oaidl.ICreateTypeLib.SetDocString
title: ICreateTypeLib::SetDocString method
author: windows-driver-content
description: Sets the documentation string associated with the library.
old-location: automat\icreatetypelib_setdocstring.htm
old-project: automat
ms.assetid: 5fe93ad2-f3c2-4559-a64a-cbbc17448e05
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: ICreateTypeLib, ICreateTypeLib interface [Automation], SetDocString method, ICreateTypeLib::SetDocString, SetDocString method [Automation], SetDocString method [Automation], ICreateTypeLib interface, SetDocString,ICreateTypeLib.SetDocString, _oa96_ICreateTypeLib_SetDocString, automat.icreatetypelib_setdocstring, oaidl/ICreateTypeLib::SetDocString
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
-	ICreateTypeLib.SetDocString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ICreateTypeLib::SetDocString method


## -description


Sets the documentation string associated with the library.


## -parameters




### -param szDoc [in]

A brief description of the type library.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



The documentation string is a brief description of the library intended for use by type information browsing tools.





## -see-also




<a href="https://msdn.microsoft.com/d245cd25-ce31-42da-a42d-dc412d5b98e7">ICreateTypeLib</a>
 

 

