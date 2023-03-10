---
UID: NF:oleauto.DispInvoke
title: DispInvoke function (oleauto.h)
description: Automatically calls member functions on an interface, given the type information for the interface.
helpviewer_keywords: ["DISPATCH_METHOD","DISPATCH_PROPERTYGET","DISPATCH_PROPERTYPUT","DISPATCH_PROPERTYPUTREF","DispInvoke","DispInvoke function [Automation]","_oa96_DispInvoke","automat.dispinvoke","oleauto/DispInvoke"]
old-location: automat\dispinvoke.htm
tech.root: automat
ms.assetid: 69b89e5c-2a04-4a6a-beb0-18e68f8866ac
ms.date: 12/05/2018
ms.keywords: DISPATCH_METHOD, DISPATCH_PROPERTYGET, DISPATCH_PROPERTYPUT, DISPATCH_PROPERTYPUTREF, DispInvoke, DispInvoke function [Automation], _oa96_DispInvoke, automat.dispinvoke, oleauto/DispInvoke
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DispInvoke
 - oleauto/DispInvoke
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - DispInvoke
---

# DispInvoke function


## -description

Automatically calls member functions on an interface, given the type information for the interface. You can describe an interface with type information and implement <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">Invoke</a> for the interface using this single call.

## -parameters

### -param _this

An implementation of the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface described by <i>ptinfo</i>.

### -param ptinfo

The type information that describes the interface.

### -param dispidMember

The member to be invoked. Use <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames">GetIDsOfNames</a> or the object's documentation to obtain the DISPID.

### -param wFlags

Flags describing the context of the <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">Invoke</a> call.

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
The member is invoked as a method. If a property has the same name, both this and the DISPATCH_PROPERTYGET flag can be set.


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
The member is changed by a reference assignment, rather than a value assignment. This flag is valid only when the property accepts a reference to an object.


</td>
</tr>
</table>

### -param pparams

Pointer to a structure containing an array of arguments, an array of argument DISPIDs for named arguments, and counts for number of elements in the arrays.

### -param pvarResult

Pointer to where the result is to be stored, or Null if the caller expects no result. This argument is ignored if DISPATCH_PROPERTYPUT or DISPATCH_PROPERTYPUTREF is specified.

### -param pexcepinfo

Pointer to a structure containing exception information. This structure should be filled in if DISP_E_EXCEPTION is returned.

### -param puArgErr

The index within rgvarg of the first argument that has an error. Arguments are stored in pdispparams-&gt;rgvarg in reverse order, so the first argument is the one with the highest index in the array. This parameter is returned only when the resulting return value is DISP_E_TYPEMISMATCH or DISP_E_PARAMNOTFOUND.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BADPARAMCOUNT</b></dt>
</dl>
</td>
<td width="60%">
The number of elements provided to DISPPARAMS is different from the number of arguments accepted by the method or property.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BADVARTYPE</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments in DISPPARAMS is not a valid variant type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
The application needs to raise an exception. In this case, the structure passed in <i>pexcepinfo</i> should be filled in.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_MEMBERNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested member does not exist.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_NONAMEDARGS</b></dt>
</dl>
</td>
<td width="60%">
This implementation of <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> does not support named arguments.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments in DISPPARAMS could not be coerced to the specified type.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_PARAMNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter IDs does not correspond to a parameter on the method. In this case, <i>puArgErr</i> is set to the first argument that contains the error.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_PARAMNOTOPTIONAL</b></dt>
</dl>
</td>
<td width="60%">
A required parameter was omitted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments could not be coerced. The index of the first parameter with the incorrect type within rgvarg is returned in <i>puArgErr</i>.


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
One of the parameters is not valid.

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
 

Any of the <b>ITypeInfo::Invoke</b> errors can also be returned.

## -remarks

The parameter <i>_this</i> is a pointer to an implementation of the interface that is being deferred to. <b>DispInvoke</b> builds a stack frame, coerces parameters using standard coercion rules, pushes them on the stack, and then calls the correct member function in the VTBL.


#### Examples

The following code from the Lines sample file Lines.cpp implements <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">Invoke</a> using <b>DispInvoke</b>. This implementation relies on <b>DispInvoke</b> to validate input arguments. To help minimize security risks, include code that performs more robust validation of the input arguments.


```cpp
STDMETHODIMP
CLines::Invoke(
   DISPID dispidMember,
   REFIID riid,
   LCID lcid,
   WORD wFlags,
   DISPPARAMS * pdispparams,
   VARIANT * pvarResult,
   EXCEPINFO* pexcepinfo,
   UINT * puArgErr)
{
   return DispInvoke(
   this, m_ptinfo,
   dispidMember, wFlags, pdispparams,
   pvarResult, pexcepinfo, puArgErr); 
}
```

## -see-also

<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createstddispatch">CreateStdDispatch</a>



<a href="/previous-versions/windows/desktop/automat/dispatch-functions">Creation of Dispatch API Functions</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">IDispatch::Invoke</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke">ITypeInfo::Invoke</a>