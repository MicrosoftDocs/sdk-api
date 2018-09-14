---
UID: NF:oaidl.ITypeInfo.GetIDsOfNames
title: ITypeInfo::GetIDsOfNames
author: windows-sdk-content
description: Maps between member names and member IDs, and parameter names and parameter IDs.
old-location: automat\itypeinfo_getidsofnames.htm
tech.root: automat
ms.assetid: fb66ee55-e491-40e9-a795-58beb4acee25
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetIDsOfNames, GetIDsOfNames method [Automation], GetIDsOfNames method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetIDsOfNames method, ITypeInfo.GetIDsOfNames, ITypeInfo2.GetIDsOfNames, ITypeInfo::GetIDsOfNames, _oa96_ITypeInfo_GetIDsOfNames, automat.itypeinfo_getidsofnames, oaidl/ITypeInfo::GetIDsOfNames
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
 - oleaut32.dll
api_name:
 - ITypeInfo.GetIDsOfNames
 - ITypeInfo2.GetIDsOfNames
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITypeInfo::GetIDsOfNames


## -description


Maps between member names and member IDs, and parameter names and parameter IDs.


## -parameters




### -param rgszNames [in]

An array of names to be mapped.




### -param cNames [in]

The count of the names to be mapped.


### -param pMemId [out]

Caller-allocated array in which name mappings are placed.


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



The function <a href="https://msdn.microsoft.com/6f6cf233-3481-436e-8d6a-51f93bf91619">GetIDsOfNames</a> maps the name of a member (<b>rgszNames</b>[0]) and its parameters (<b>rgszNames</b>[1] ...<b>rgszNames</b>[<b>cNames</b>- 1]) to the ID of the member (<b>pMemId</b>[0]), and to the IDs of the specified parameters (<b>pMemId</b>[1] ... <b>pMemId</b>[<b>cNames</b>- 1]). The IDs of parameters are 0 for the first parameter in the member function's argument list, 1 for the second, and so on.



If the type description inherits from another type description, this function is recursive to the base type description, if necessary, to find the item with the requested member ID.





## -see-also




<a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>
 

 

