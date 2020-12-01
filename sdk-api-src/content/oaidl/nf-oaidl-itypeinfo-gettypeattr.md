---
UID: NF:oaidl.ITypeInfo.GetTypeAttr
title: ITypeInfo::GetTypeAttr (oaidl.h)
description: Retrieves a TYPEATTR structure that contains the attributes of the type description.
helpviewer_keywords: ["GetTypeAttr","GetTypeAttr method [Automation]","GetTypeAttr method [Automation]","ITypeInfo interface","ITypeInfo interface [Automation]","GetTypeAttr method","ITypeInfo.GetTypeAttr","ITypeInfo::GetTypeAttr","_oa96_ITypeInfo_GetTypeAttr","automat.itypeinfo_gettypeattr","oaidl/ITypeInfo::GetTypeAttr"]
old-location: automat\itypeinfo_gettypeattr.htm
tech.root: automat
ms.assetid: 62be8a38-1d51-4b54-b224-7d9cdbb1be59
ms.date: 12/05/2018
ms.keywords: GetTypeAttr, GetTypeAttr method [Automation], GetTypeAttr method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetTypeAttr method, ITypeInfo.GetTypeAttr, ITypeInfo::GetTypeAttr, _oa96_ITypeInfo_GetTypeAttr, automat.itypeinfo_gettypeattr, oaidl/ITypeInfo::GetTypeAttr
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
 - ITypeInfo::GetTypeAttr
 - oaidl/ITypeInfo::GetTypeAttr
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
 - ITypeInfo.GetTypeAttr
---

# ITypeInfo::GetTypeAttr


## -description

Retrieves a TYPEATTR structure that contains the attributes of the type description.

## -parameters

### -param ppTypeAttr [out]

The attributes of this type description.

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

To free the TYPEATTR structure, use <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-releasetypeattr">ITypeInfo::ReleaseTypeAttr</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>