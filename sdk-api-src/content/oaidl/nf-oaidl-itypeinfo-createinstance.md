---
UID: NF:oaidl.ITypeInfo.CreateInstance
title: ITypeInfo::CreateInstance (oaidl.h)
description: Creates a new instance of a type that describes a component object class (coclass).
helpviewer_keywords: ["CreateInstance","CreateInstance method [Automation]","CreateInstance method [Automation]","ITypeInfo interface","ITypeInfo interface [Automation]","CreateInstance method","ITypeInfo.CreateInstance","ITypeInfo::CreateInstance","_oa96_ITypeInfo_CreateInstance","automat.itypeinfo_createinstance","oaidl/ITypeInfo::CreateInstance"]
old-location: automat\itypeinfo_createinstance.htm
tech.root: automat
ms.assetid: b11c51e6-8ae7-482d-87eb-8175ca98eb63
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [Automation], CreateInstance method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],CreateInstance method, ITypeInfo.CreateInstance, ITypeInfo::CreateInstance, _oa96_ITypeInfo_CreateInstance, automat.itypeinfo_createinstance, oaidl/ITypeInfo::CreateInstance
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
 - ITypeInfo::CreateInstance
 - oaidl/ITypeInfo::CreateInstance
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
 - ITypeInfo.CreateInstance
---

# ITypeInfo::CreateInstance


## -description

Creates a new instance of a type that describes a component object class (coclass).

## -parameters

### -param pUnkOuter [in]

The controlling <b>IUnknown</b>. If Null, then a stand-alone instance is created. If valid, then an aggregate object is created.

### -param riid [in]

An ID for the interface that the caller will use to communicate with the resulting object.

### -param ppvObj [out]

An instance of the created object.

## -returns

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
 

Additional errors may be returned from <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-getactiveobject">GetActiveObject</a> or <b>CoCreateInstance</b>.

## -remarks

For types that describe a component object class (coclass), <b>CreateInstance</b> creates a new instance of the class. Normally, <b>CreateInstance</b> calls <b>CoCreateInstance</b> with the type description's GUID. For an Application object, it first calls <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-getactiveobject">GetActiveObject</a>. If the application is active, <b>GetActiveObject</b> returns the active object; otherwise, if <b>GetActiveObject</b> fails, <b>CreateInstance</b> calls <b>CoCreateInstance</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>