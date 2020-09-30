---
UID: NF:oaidl.ITypeInfo.GetTypeComp
title: ITypeInfo::GetTypeComp (oaidl.h)
description: Retrieves the ITypeComp interface for the type description, which enables a client compiler to bind to the type description's members.
helpviewer_keywords: ["GetTypeComp","GetTypeComp method [Automation]","GetTypeComp method [Automation]","ITypeInfo interface","ITypeInfo interface [Automation]","GetTypeComp method","ITypeInfo.GetTypeComp","ITypeInfo::GetTypeComp","_oa96_ITypeInfo_GetTypeComp","automat.itypeinfo_gettypecomp","oaidl/ITypeInfo::GetTypeComp"]
old-location: automat\itypeinfo_gettypecomp.htm
tech.root: automat
ms.assetid: 094cf9d5-2d9b-4c3c-844e-45737e905099
ms.date: 12/05/2018
ms.keywords: GetTypeComp, GetTypeComp method [Automation], GetTypeComp method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetTypeComp method, ITypeInfo.GetTypeComp, ITypeInfo::GetTypeComp, _oa96_ITypeInfo_GetTypeComp, automat.itypeinfo_gettypecomp, oaidl/ITypeInfo::GetTypeComp
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
 - ITypeInfo::GetTypeComp
 - oaidl/ITypeInfo::GetTypeComp
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
 - ITypeInfo.GetTypeComp
---

# ITypeInfo::GetTypeComp


## -description

Retrieves the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a> interface for the type description, which enables a client compiler to bind to the type description's members.

## -parameters

### -param ppTComp [out]

The <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a> of the containing type library.

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

A client compiler can use the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a> interface to bind to members of the type.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>