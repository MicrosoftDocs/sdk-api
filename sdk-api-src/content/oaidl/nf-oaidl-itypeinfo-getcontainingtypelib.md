---
UID: NF:oaidl.ITypeInfo.GetContainingTypeLib
title: ITypeInfo::GetContainingTypeLib
author: windows-sdk-content
description: Retrieves the containing type library and the index of the type description within that type library.
old-location: automat\itypeinfo_getcontainingtypelib.htm
old-project: automat
ms.assetid: 9ca58285-4778-4c2a-b800-dcda9b62e328
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: GetContainingTypeLib, GetContainingTypeLib method [Automation], GetContainingTypeLib method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetContainingTypeLib method, ITypeInfo.GetContainingTypeLib, ITypeInfo::GetContainingTypeLib, _oa96_ITypeInfo_GetContainingTypeLib, automat.itypeinfo_getcontainingtypelib, oaidl/ITypeInfo::GetContainingTypeLib
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
 - ITypeInfo.GetContainingTypeLib
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITypeInfo::GetContainingTypeLib


## -description


Retrieves the containing type library and the index of the type description within that type library.


## -parameters




### -param ppTLib [out]

The containing type library.


### -param pIndex [out]

The index of the type description within the containing type library.


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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
OLE could not find an implementation of one or more required interfaces.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>
 

 

