---
UID: NF:oaidl.ITypeInfo.Invoke
title: ITypeInfo::Invoke (oaidl.h)
description: Invokes a method, or accesses a property of an object, that implements the interface described by the type description.
helpviewer_keywords: ["DISPATCH_METHOD","DISPATCH_PROPERTYGET","DISPATCH_PROPERTYPUT","DISPATCH_PROPERTYPUTREF","ITypeInfo interface [Automation]","Invoke method","ITypeInfo.Invoke","ITypeInfo2.Invoke","ITypeInfo::Invoke","Invoke","Invoke method [Automation]","Invoke method [Automation]","ITypeInfo interface","_oa96_ITypeInfo_Invoke","automat.itypeinfo_invoke","oaidl/ITypeInfo::Invoke"]
old-location: automat\itypeinfo_invoke.htm
tech.root: automat
ms.assetid: dde2ca58-84bd-4a49-a160-a9955d691f3b
ms.date: 12/05/2018
ms.keywords: DISPATCH_METHOD, DISPATCH_PROPERTYGET, DISPATCH_PROPERTYPUT, DISPATCH_PROPERTYPUTREF, ITypeInfo interface [Automation],Invoke method, ITypeInfo.Invoke, ITypeInfo2.Invoke, ITypeInfo::Invoke, Invoke, Invoke method [Automation], Invoke method [Automation],ITypeInfo interface, _oa96_ITypeInfo_Invoke, automat.itypeinfo_invoke, oaidl/ITypeInfo::Invoke
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
 - ITypeInfo::Invoke
 - oaidl/ITypeInfo::Invoke
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
 - oleaut32.dll
api_name:
 - ITypeInfo.Invoke
 - ITypeInfo2.Invoke
---

# ITypeInfo::Invoke


## -description

Invokes a method, or accesses a property of an object, that implements the interface described by the type description.

## -parameters

### -param pvInstance [in]

An instance of the interface described by this type description.

### -param memid [in]

The interface member.

### -param wFlags [in]

Flags describing the context of the invoke call.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISPATCH_METHOD"></a><a id="dispatch_method"></a><dl>
<dt><b>DISPATCH_METHOD</b></dt>
</dl>
</td>
<td width="60%">
The member is accessed as a method. If there is ambiguity, both this and the DISPATCH_PROPERTYGET flag can be set.


</td>
</tr>
<tr>
<td width="40%"><a id="DISPATCH_PROPERTYGET"></a><a id="dispatch_propertyget"></a><dl>
<dt><b>DISPATCH_PROPERTYGET</b></dt>
</dl>
</td>
<td width="60%">
The member is retrieved as a property or data member.


</td>
</tr>
<tr>
<td width="40%"><a id="DISPATCH_PROPERTYPUT"></a><a id="dispatch_propertyput"></a><dl>
<dt><b>DISPATCH_PROPERTYPUT</b></dt>
</dl>
</td>
<td width="60%">
The member is changed as a property or data member.


</td>
</tr>
<tr>
<td width="40%"><a id="DISPATCH_PROPERTYPUTREF"></a><a id="dispatch_propertyputref"></a><dl>
<dt><b>DISPATCH_PROPERTYPUTREF</b></dt>
</dl>
</td>
<td width="60%">
The member is changed by using a reference assignment, rather than a value assignment. This flag is valid only when the property accepts a reference to an object.


</td>
</tr>
</table>

### -param pDispParams [in, out]

An array of arguments, an array of DISPIDs for named arguments, and counts of the number of elements in each array.

### -param pVarResult [out]

The result. Should be null if the caller does not expect any result. If <i>wFlags</i> specifies DISPATCH_PROPERTYPUT or DISPATCH_PROPERTYPUTREF, <i>pVarResultis</i> is ignored.

### -param pExcepInfo [out]

An exception information structure, which is filled in only if DISP_E_EXCEPTION is returned. If <i>pExcepInfo</i> is null on input, only an HRESULT error will be returned.

### -param puArgErr [out]

If Invoke returns DISP_E_TYPEMISMATCH, <i>puArgErr</i> indicates the index (within <i>rgvarg</i>) of the argument with incorrect type. If more than one argument returns an error, <i>puArgErr</i> indicates only the first argument with an error. Arguments in pDispParams-&gt;rgvarg appear in reverse order, so the first argument is the one having the highest index in the array. This parameter cannot be null.

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
<dt><b>DISP_E_EXCEPTION
</b></dt>
</dl>
</td>
<td width="60%">
The member being invoked has returned an error HRESULT. If the member implements <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo">IErrorInfo</a>, details are available in the error object. Otherwise, the <i>pExcepInfo</i> parameter contains details. 

</td>
</tr>
</table>
 

Any of the <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">IDispatch::Invoke</a> errors may also be returned.

## -remarks

Use the function <b>ITypeInfo::Invoke</b> to access a member of an object or invoke a method that implements the interface described by this type description. For objects that support the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface, you can use <b>Invoke</b> to implement <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">IDispatch::Invoke</a>.



<b>ITypeInfo::Invoke</b> takes a pointer to an instance of the class. Otherwise, its parameters are the same as <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">IDispatch::Invoke</a>, except that <b>ITypeInfo::Invoke</b> omits the <i>refiid</i> and <i>lcid</i> parameters. When called, <b>ITypeInfo::Invoke</b> performs the actions described by the <b>IDispatch::Invoke</b> parameters on the specified instance.



For VTBL interface members, <b>ITypeInfo::Invoke</b> passes the LCID of the type information into parameters tagged with the lcid attribute, and the returned value into the retval attribute.



If the type description inherits from another type description, this function recurses on the base type description to find the item with the requested member ID.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>