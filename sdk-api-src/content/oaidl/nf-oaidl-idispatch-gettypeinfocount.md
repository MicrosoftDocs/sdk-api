---
UID: NF:oaidl.IDispatch.GetTypeInfoCount
title: IDispatch::GetTypeInfoCount (oaidl.h)
description: Retrieves the number of type information interfaces that an object provides (either 0 or 1).
helpviewer_keywords: ["GetTypeInfoCount","GetTypeInfoCount method [Automation]","GetTypeInfoCount method [Automation]","IAccessible interface","GetTypeInfoCount method [Automation]","IDispatch interface","IAccessible interface [Automation]","GetTypeInfoCount method","IAccessible::GetTypeInfoCount","IDispatch interface [Automation]","GetTypeInfoCount method","IDispatch.GetTypeInfoCount","IDispatch::GetTypeInfoCount","_oa96_IDispatch::GetTypeInfoCount","automat.idispatch_gettypeinfocount","oaidl/IAccessible::GetTypeInfoCount","oaidl/IDispatch::GetTypeInfoCount"]
old-location: automat\idispatch_gettypeinfocount.htm
tech.root: automat
ms.assetid: da876d53-cb8a-465c-a43e-c0eb272e2a12
ms.date: 12/05/2018
ms.keywords: GetTypeInfoCount, GetTypeInfoCount method [Automation], GetTypeInfoCount method [Automation],IAccessible interface, GetTypeInfoCount method [Automation],IDispatch interface, IAccessible interface [Automation],GetTypeInfoCount method, IAccessible::GetTypeInfoCount, IDispatch interface [Automation],GetTypeInfoCount method, IDispatch.GetTypeInfoCount, IDispatch::GetTypeInfoCount, _oa96_IDispatch::GetTypeInfoCount, automat.idispatch_gettypeinfocount, oaidl/IAccessible::GetTypeInfoCount, oaidl/IDispatch::GetTypeInfoCount
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
 - IDispatch::GetTypeInfoCount
 - oaidl/IDispatch::GetTypeInfoCount
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
 - IDispatch.GetTypeInfoCount
 - IAccessible.GetTypeInfoCount
---

# IDispatch::GetTypeInfoCount


## -description

Retrieves the number of type information interfaces that an object provides (either 0 or 1).

## -parameters

### -param pctinfo [out]

The number of type information interfaces provided by the object. If the object provides type information, this number is 1; otherwise the number is 0.

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
<dt><b>E_NOTIMPL
</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
</table>

## -remarks

The method may return zero, which indicates that the object does not provide any type information. In this case, the object may still be programmable through <b>IDispatch</b> or a VTBL, but does not provide run-time type information for browsers, compilers, or other programming tools that access type information. This can be useful for hiding an object from browsers.


#### Examples

This code from the Lines sample file Lines.cpp implements the <b>GetTypeInfoCount</b> member function for the <b>CLines</b> class (ActiveX or OLE object).


```cpp
STDMETHODIMP
CLines::GetTypeInfoCount(UINT * pctinfo)
{
   if (pctinfo == NULL) {
      return E_INVALIDARG;
}
   *pctinfo = 1;
   return NOERROR;
}
```

## -see-also

<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>