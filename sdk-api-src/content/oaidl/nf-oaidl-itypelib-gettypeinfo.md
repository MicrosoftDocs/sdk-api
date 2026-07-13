---
UID: NF:oaidl.ITypeLib.GetTypeInfo
title: ITypeLib::GetTypeInfo (oaidl.h)
description: Retrieves the specified type description in the library.
helpviewer_keywords: ["GetTypeInfo","GetTypeInfo method [Automation]","GetTypeInfo method [Automation]","ITypeLib interface","ITypeLib interface [Automation]","GetTypeInfo method","ITypeLib.GetTypeInfo","ITypeLib::GetTypeInfo","_oa96_ITypeLib_GetTypeInfo","automat.itypelib_gettypeinfo","oaidl/ITypeLib::GetTypeInfo"]
old-location: automat\itypelib_gettypeinfo.htm
tech.root: automat
ms.assetid: 7661faa8-eb06-4bbe-88e9-9662a0d6984b
ms.date: 12/05/2018
ms.keywords: GetTypeInfo, GetTypeInfo method [Automation], GetTypeInfo method [Automation],ITypeLib interface, ITypeLib interface [Automation],GetTypeInfo method, ITypeLib.GetTypeInfo, ITypeLib::GetTypeInfo, _oa96_ITypeLib_GetTypeInfo, automat.itypelib_gettypeinfo, oaidl/ITypeLib::GetTypeInfo
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
 - ITypeLib::GetTypeInfo
 - oaidl/ITypeLib::GetTypeInfo
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
 - ITypeLib.GetTypeInfo
---

# ITypeLib::GetTypeInfo


## -description

Retrieves the specified type description in the library.

## -parameters

### -param index [in]

The index of the interface to be returned.

### -param ppTInfo [out]

If successful, returns a pointer to the pointer to the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a> interface.

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
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The <i>index</i> parameter is outside the range of  to <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-gettypeinfocount">GetTypeInfoCount</a> - 1.

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

For dual interfaces, <b>GetTypeInfo</b> returns only the TKIND_DISPATCH type information. To get the TKIND_INTERFACE type information, <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getreftypeofimpltype">GetRefTypeOfImplType</a> can be called on the TKIND_DISPATCH type information, passing an index of –1. Then, the returned type information handle can be passed to <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-getreftypeinfo">GetRefTypeInfo</a>.


#### Examples

The following example gets the TKIND_INTERFACE type information for a dual interface.


```cpp
HRESULT hr;
hr = ptlib->GetTypeInfo((unsigned int) dwIndex, &ptypeinfoDisp);
if (FAILED(hr)) {
   //free resources
   return hr;
}
hr = ptypeinfoDisp->GetRefTypeOfImplType(-1, &phreftype);
if (FAILED(hr)) {
   //free resources
   return hr;

hr = ptypeinfoDisp->GetRefTypeInfo(phreftype, &ptypeinfoInt);
if (FAILED(hr)) {
   //free resources
   return hr;

// 
```

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypelib">ITypeLib</a>