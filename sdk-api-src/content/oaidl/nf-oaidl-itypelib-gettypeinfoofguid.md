---
UID: NF:oaidl.ITypeLib.GetTypeInfoOfGuid
title: ITypeLib::GetTypeInfoOfGuid
author: windows-sdk-content
description: Retrieves the type description that corresponds to the specified GUID.
old-location: automat\itypelib_gettypeinfoofguid.htm
tech.root: automat
ms.assetid: 58f96322-f1cd-448c-906d-b7faa65ab9a0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTypeInfoOfGuid, GetTypeInfoOfGuid method [Automation], GetTypeInfoOfGuid method [Automation],ITypeLib interface, ITypeLib interface [Automation],GetTypeInfoOfGuid method, ITypeLib.GetTypeInfoOfGuid, ITypeLib::GetTypeInfoOfGuid, _oa96_ITypeLib_GetTypeInfoOfGuid, automat.itypelib_gettypeinfoofguid, oaidl/ITypeLib::GetTypeInfoOfGuid
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
 - ITypeLib.GetTypeInfoOfGuid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITypeLib::GetTypeInfoOfGuid


## -description


Retrieves the type description that corresponds to the specified GUID.


## -parameters




### -param guid [in]

The GUID of the type description.


### -param ppTinfo [out]

The <a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a> interface.


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
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
No type description was found in the library with the specified GUID.

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




<a href="https://msdn.microsoft.com/c1e5d71f-6a4e-45f3-811d-f57024f81a55">ITypeLib</a>
 

 

