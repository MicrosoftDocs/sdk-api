---
UID: NF:oaidl.ITypeInfo.AddressOfMember
title: ITypeInfo::AddressOfMember (oaidl.h)
description: Retrieves the addresses of static functions or variables, such as those defined in a DLL.
helpviewer_keywords: ["AddressOfMember","AddressOfMember method [Automation]","AddressOfMember method [Automation]","ITypeInfo interface","ITypeInfo interface [Automation]","AddressOfMember method","ITypeInfo.AddressOfMember","ITypeInfo::AddressOfMember","_oa96_ITypeInfo_AddressOfMember","automat.itypeinfo_addressofmember","oaidl/ITypeInfo::AddressOfMember"]
old-location: automat\itypeinfo_addressofmember.htm
tech.root: automat
ms.assetid: cf351457-13ff-4e40-9d92-89c6db42627c
ms.date: 12/05/2018
ms.keywords: AddressOfMember, AddressOfMember method [Automation], AddressOfMember method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],AddressOfMember method, ITypeInfo.AddressOfMember, ITypeInfo::AddressOfMember, _oa96_ITypeInfo_AddressOfMember, automat.itypeinfo_addressofmember, oaidl/ITypeInfo::AddressOfMember
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITypeInfo::AddressOfMember
 - oaidl/ITypeInfo::AddressOfMember
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ITypeInfo.AddressOfMember
---

# ITypeInfo::AddressOfMember


## -description

Retrieves the addresses of static functions or variables, such as those defined in a DLL.

## -parameters

### -param memid [in]

The member ID of the static member whose address is to be retrieved. The member ID is defined by the DISPID.

### -param invKind [in]

Indicates whether the member is a property, and if so, what kind.

### -param ppv [out]

The static member.

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

The addresses are valid until the caller releases its reference to the type description. The <i>invKind</i> parameter can be ignored unless the address of a property function is being requested.

If the type description inherits from another type description, this function is recursive to the base type description, if necessary, to find the item with the requested member ID.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>