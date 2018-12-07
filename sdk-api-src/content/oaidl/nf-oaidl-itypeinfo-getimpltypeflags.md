---
UID: NF:oaidl.ITypeInfo.GetImplTypeFlags
title: ITypeInfo::GetImplTypeFlags
author: windows-sdk-content
description: Retrieves the IMPLTYPEFLAGS enumeration for one implemented interface or base interface in a type description.
old-location: automat\itypeinfo_getimpltypeflags.htm
tech.root: automat
ms.assetid: b3773111-b09d-4ae0-9a91-3c4adff5b803
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetImplTypeFlags, GetImplTypeFlags method [Automation], GetImplTypeFlags method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetImplTypeFlags method, ITypeInfo.GetImplTypeFlags, ITypeInfo::GetImplTypeFlags, _oa96_ITypeInfo_GetImplTypeFlags, automat.itypeinfo_getimpltypeflags, oaidl/ITypeInfo::GetImplTypeFlags
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
 - ITypeInfo.GetImplTypeFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITypeInfo::GetImplTypeFlags


## -description


Retrieves the IMPLTYPEFLAGS enumeration for one implemented interface or base interface in a type description.


## -parameters




### -param index [in]

The index of the implemented interface or base interface for which to get the flags.




### -param pImplTypeFlags [out]

The IMPLTYPEFLAGS enumeration value.


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



The flags are associated with the act of inheritance, and not with the inherited interface.





## -see-also




<a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>
 

 

