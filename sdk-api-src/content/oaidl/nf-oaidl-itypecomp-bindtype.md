---
UID: NF:oaidl.ITypeComp.BindType
title: ITypeComp::BindType (oaidl.h)
description: Binds to the type descriptions contained within a type library.
helpviewer_keywords: ["BindType","BindType method [Automation]","BindType method [Automation]","ITypeComp interface","ITypeComp interface [Automation]","BindType method","ITypeComp.BindType","ITypeComp::BindType","_oa96_ITypeComp_BindType","automat.itypecomp_bindtype","oaidl/ITypeComp::BindType"]
old-location: automat\itypecomp_bindtype.htm
tech.root: automat
ms.assetid: e1b6eb9c-aa5a-41b9-bc97-afa82206ccef
ms.date: 12/05/2018
ms.keywords: BindType, BindType method [Automation], BindType method [Automation],ITypeComp interface, ITypeComp interface [Automation],BindType method, ITypeComp.BindType, ITypeComp::BindType, _oa96_ITypeComp_BindType, automat.itypecomp_bindtype, oaidl/ITypeComp::BindType
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
 - ITypeComp::BindType
 - oaidl/ITypeComp::BindType
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
 - ITypeComp.BindType
---

# ITypeComp::BindType


## -description

Binds to the type descriptions contained within a type library.

## -parameters

### -param szName [in]

The name to be bound.

### -param lHashVal [in]

The hash value for the name computed by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-lhashvalofname">LHashValOfName</a>.

### -param ppTInfo [out]

 An <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a> of the type to which the name was bound.

### -param ppTComp [out]

Passes a valid pointer, such as the address of an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a> variable.

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

Use the function <b>BindType</b> for binding a type name to the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a> that describes the type. This function is invoked on the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a> that is returned by <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-gettypecomp">ITypeLib::GetTypeComp</a> to bind to types defined within that library. It can also be used in the future for binding to nested types.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a>