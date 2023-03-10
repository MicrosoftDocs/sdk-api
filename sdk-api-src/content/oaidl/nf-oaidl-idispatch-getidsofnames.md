---
UID: NF:oaidl.IDispatch.GetIDsOfNames
title: IDispatch::GetIDsOfNames (oaidl.h)
description: Maps a single member and an optional set of argument names to a corresponding set of integer DISPIDs, which can be used on subsequent calls to Invoke.
helpviewer_keywords: ["GetIDsOfNames","GetIDsOfNames method [Automation]","GetIDsOfNames method [Automation]","IDispatch interface","IDispatch interface [Automation]","GetIDsOfNames method","IDispatch.GetIDsOfNames","IDispatch::GetIDsOfNames","_oa96_IDispatch::GetIDsOfNames","automat.idispatch_getidsofnames","oaidl/IDispatch::GetIDsOfNames"]
old-location: automat\idispatch_getidsofnames.htm
tech.root: automat
ms.assetid: 6f6cf233-3481-436e-8d6a-51f93bf91619
ms.date: 12/05/2018
ms.keywords: GetIDsOfNames, GetIDsOfNames method [Automation], GetIDsOfNames method [Automation],IDispatch interface, IDispatch interface [Automation],GetIDsOfNames method, IDispatch.GetIDsOfNames, IDispatch::GetIDsOfNames, _oa96_IDispatch::GetIDsOfNames, automat.idispatch_getidsofnames, oaidl/IDispatch::GetIDsOfNames
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
 - IDispatch::GetIDsOfNames
 - oaidl/IDispatch::GetIDsOfNames
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
 - IDispatch.GetIDsOfNames
---

# IDispatch::GetIDsOfNames


## -description

Maps a single member and an optional set of argument names to a corresponding set of integer DISPIDs, which can be used on subsequent calls to <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">Invoke</a>. The dispatch function <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames">DispGetIDsOfNames</a> provides a standard implementation of <b>GetIDsOfNames</b>.

## -parameters

### -param riid [in]

Reserved for future use. Must be IID_NULL.

### -param rgszNames [in]

The array of names to be mapped.

### -param cNames [in]

The count of the names to be mapped.

### -param lcid [in]

The locale context in which to interpret the names.

### -param rgDispId [out]

Caller-allocated array, each element of which contains an identifier (ID) corresponding to one of the names passed in the rgszNames array. The first element represents the member name. The subsequent elements represent each of the member's parameters.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_UNKNOWNNAME</b></dt>
</dl>
</td>
<td width="60%">
One or more of the specified names were not known. The returned array of DISPIDs contains DISPID_UNKNOWN for each entry that corresponds to an unknown name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_UNKNOWNLCID</b></dt>
</dl>
</td>
<td width="60%">
The locale identifier (LCID) was not recognized.


</td>
</tr>
</table>

## -remarks

An <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> implementation can associate any positive integer ID value with a given name. Zero is reserved for the default, or <b>Value</b> property; –1 is reserved to indicate an unknown name; and other negative values are defined for other purposes. For example, if <b>GetIDsOfNames</b> is called, and the implementation does not recognize one or more of the names, it returns DISP_E_UNKNOWNNAME, and the <i>rgDispId</i> array contains DISPID_UNKNOWN for the entries that correspond to the unknown names.

The member and parameter DISPIDs must remain constant for the lifetime of the object. This allows a client to obtain the DISPIDs once, and cache them for later use.

When <b>GetIDsOfNames</b> is called with more than one name, the first name (<i>rgszNames</i>[0]) corresponds to the member name, and subsequent names correspond to the names of the member's parameters.

The same name may map to different DISPIDs, depending on context. For example, a name may have a DISPID when it is used as a member name with a particular interface, a different ID as a member of a different interface, and different mapping for each time it appears as a parameter.

<b>GetIDsOfNames</b> is used when an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> client binds to names at run time. To bind at compile time instead, an <b>IDispatch</b> client can map names to DISPIDs by using the type information interfaces described in <a href="/previous-versions/windows/desktop/automat/type-description-interfaces">Type Description Interfaces</a>. This allows a client to bind to members at compile time and avoid calling <b>GetIDsOfNames</b> at run time. For a description of binding at compile time, see Type Description Interfaces. 

The implementation of <b>GetIDsOfNames</b> is case insensitive. Users that need case-sensitive name mapping should use type information interfaces to map names to DISPIDs, rather than call <b>GetIDsOfNames</b>.

<div class="alert"><b>Caution</b>  You cannot use this method to access values that have been added dynamically, such as values added through JavaScript. Instead, use the GetDispID of the IDispatchEx interface. For more information, see the <a href="/previous-versions/windows/internet-explorer/ie-developer/windows-scripting/reference/idispatchex-interface">IDispatchEx interface</a>.</div>
<div> </div>

#### Examples

The following code from the Lines sample file Lines.cpp implements the <b>GetIDsOfNames</b> member function for the CLine class. The ActiveX or OLE object uses the standard implementation, <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames">DispGetIDsOfNames</a>. This implementation relies on <b>DispGetIdsOfNames</b> to validate input arguments. To help minimize security risks, include code that performs more robust validation of the input arguments.


```cpp
STDMETHODIMP 
CLine::GetIDsOfNames(
      REFIID riid,
      OLECHAR ** rgszNames,
      UINT cNames,
      LCID lcid,
      DISPID * rgDispId)
{
      return DispGetIDsOfNames(m_ptinfo, rgszNames, cNames, rgDispId);
}
```


The following code might appear in an ActiveX client that calls <b>GetIDsOfNames</b> to get the DISPID of the <b>CLine</b><b>Color</b> property.


```cpp
HRESULT hresult;
IDispatch * pdisp = (IDispatch *)NULL;
DISPID dispid;
OLECHAR * szMember = "color";

// Code that sets a pointer to the dispatch (pdisp) is omitted.

hresult = pdisp->GetIDsOfNames(
   IID_NULL,
   &szMember,
   1, LOCALE_SYSTEM_DEFAULT,
   &dispid);
```

## -see-also

<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createstddispatch">CreateStdDispatch</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames">DispGetIDsOfNames</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>