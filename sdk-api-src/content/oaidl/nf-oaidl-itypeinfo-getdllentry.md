---
UID: NF:oaidl.ITypeInfo.GetDllEntry
title: ITypeInfo::GetDllEntry
author: windows-sdk-content
description: Retrieves a description or specification of an entry point for a function in a DLL.
old-location: automat\itypeinfo_getdllentry.htm
old-project: automat
ms.assetid: 1b947de4-4a3e-40f3-837b-c60b0ab67ef1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDllEntry, GetDllEntry method [Automation], GetDllEntry method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetDllEntry method, ITypeInfo.GetDllEntry, ITypeInfo::GetDllEntry, _oa96_ITypeInfo_GetDllEntry, automat.itypeinfo_getdllentry, oaidl/ITypeInfo::GetDllEntry
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oaidl.h
req.include-header: 
req.redist: 
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
 - ITypeInfo.GetDllEntry
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITypeInfo::GetDllEntry


## -description


Retrieves a description or specification of an entry point for a function in a DLL.


## -parameters




### -param memid [in]

The ID of the member function whose DLL entry description is to be returned.


### -param invKind [in]

The kind of member identified by <i>memid</i>. This is important for properties, because one <i>memid</i> can identify up to three separate functions.


### -param pBstrDllName [out]

If not null, the function sets <i>pBstrDllName</i> to the name of the DLL.




### -param pBstrName [out]

If not null, the function sets <i>pBstrName</i> to the name of the entry point. If the entry point is specified by an ordinal, this argument is null.


### -param pwOrdinal [out]

If not null, and if the function is defined by an ordinal, the function sets <i>pwOrdinal</i> to the ordinal.



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



The caller passes in a member ID, which represents the member function whose entry description is desired. If the function has a DLL entry point, the name of the DLL that contains the function, as well as its name or ordinal identifier, are placed in the passed-in pointers allocated by the caller. If there is no DLL entry point for the function, an error is returned.



If the type description inherits from another type description, this function is recursive to the base type description, if necessary, to find the item with the requested member ID.



The caller should use <a href="https://msdn.microsoft.com/8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the BSTRs referenced by <i>pBstrName</i> and <i>pBstrDllName</i>.





## -see-also




<a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>
 

 

