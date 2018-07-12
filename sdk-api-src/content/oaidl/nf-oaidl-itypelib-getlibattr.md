---
UID: NF:oaidl.ITypeLib.GetLibAttr
title: ITypeLib::GetLibAttr
author: windows-sdk-content
description: Retrieves the structure that contains the library's attributes.
old-location: automat\itypelib_getlibattr.htm
old-project: automat
ms.assetid: edc35364-99dc-438b-81de-4f129c0cf50f
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: GetLibAttr, GetLibAttr method [Automation], GetLibAttr method [Automation],ITypeLib interface, ITypeLib interface [Automation],GetLibAttr method, ITypeLib.GetLibAttr, ITypeLib::GetLibAttr, _oa96_ITypeLib_GetLibAttr, automat.itypelib_getlibattr, oaidl/ITypeLib::GetLibAttr
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
 - ITypeLib.GetLibAttr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITypeLib::GetLibAttr


## -description


Retrieves the structure that contains the library's attributes.


## -parameters




### -param ppTLibAttr [out]

 The library's attributes.


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



Use <a href="https://msdn.microsoft.com/a5b9ee66-ab66-4ad9-a6bf-93bd98e3905c">ITypeLib::ReleaseTLibAttr</a> to free the memory occupied by the TLIBATTR structure.





## -see-also




<a href="https://msdn.microsoft.com/c1e5d71f-6a4e-45f3-811d-f57024f81a55">ITypeLib</a>
 

 

