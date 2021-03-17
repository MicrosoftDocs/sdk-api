---
UID: NF:oaidl.ITypeInfo.GetMops
title: ITypeInfo::GetMops (oaidl.h)
description: Retrieves marshaling information.
helpviewer_keywords: ["GetMops","GetMops method [Automation]","GetMops method [Automation]","ITypeInfo interface","ITypeInfo interface [Automation]","GetMops method","ITypeInfo.GetMops","ITypeInfo::GetMops","_oa96_ITypeInfo_GetMops","automat.itypeinfo_getmops","oaidl/ITypeInfo::GetMops"]
old-location: automat\itypeinfo_getmops.htm
tech.root: automat
ms.assetid: 6f8f4d4a-c51d-46d3-ad0f-1ee357bb7104
ms.date: 12/05/2018
ms.keywords: GetMops, GetMops method [Automation], GetMops method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetMops method, ITypeInfo.GetMops, ITypeInfo::GetMops, _oa96_ITypeInfo_GetMops, automat.itypeinfo_getmops, oaidl/ITypeInfo::GetMops
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
 - ITypeInfo::GetMops
 - oaidl/ITypeInfo::GetMops
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
 - ITypeInfo.GetMops
---

# ITypeInfo::GetMops


## -description

Retrieves marshaling information.

## -parameters

### -param memid [in]

The member ID that indicates which marshaling information is needed.

### -param pBstrMops [out]

The opcode string used in marshaling the fields of the structure described by the referenced type description, or null if there is no information to return.

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

If the passed-in member ID is MEMBERID_NIL, the function returns the opcode string for marshaling the fields of the structure described by the type description. Otherwise, it returns the opcode string for marshaling the function specified by the index.



If the type description inherits from another type description, this function recurses on the base type description, if necessary, to find the item with the requested member ID.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>