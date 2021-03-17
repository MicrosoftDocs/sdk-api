---
UID: NF:oleauto.CreateStdDispatch
title: CreateStdDispatch function (oleauto.h)
description: Creates a standard implementation of the IDispatch interface through a single function call. This simplifies exposing objects through Automation.
helpviewer_keywords: ["CreateStdDispatch","CreateStdDispatch function [Automation]","_oa96_CreateStdDispatch","automat.createstddispatch","oleauto/CreateStdDispatch"]
old-location: automat\createstddispatch.htm
tech.root: automat
ms.assetid: 45a59243-df93-41ca-ac60-354cb1165004
ms.date: 12/05/2018
ms.keywords: CreateStdDispatch, CreateStdDispatch function [Automation], _oa96_CreateStdDispatch, automat.createstddispatch, oleauto/CreateStdDispatch
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
 - CreateStdDispatch
 - oleauto/CreateStdDispatch
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
 - CreateStdDispatch
---

# CreateStdDispatch function


## -description

Creates a standard implementation of the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface through a single function call. This simplifies exposing objects through Automation.

## -parameters

### -param punkOuter

The object's <b>IUnknown</b> implementation.

### -param pvThis

The object to expose.

### -param ptinfo

The type information that describes the exposed object.

### -param ppunkStdDisp

The private unknown for the object that implements the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface QueryInterface call. This pointer is null if the function fails.

## -returns

This function can return one of these values.

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
One of the first three arguments is not valid.

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
There was insufficient memory to complete the operation.

</td>
</tr>
</table>

## -remarks

You can use <b>CreateStdDispatch</b> when creating an object instead of implementing the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> member functions for the object. However, the implementation that <b>CreateStdDispatch</b> creates has these limitations:  

<ul>
<li>
Supports only one national language.

</li>
<li>
Supports only dispatch-defined exception codes returned from <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">Invoke</a>.

</li>
</ul>

<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-loadtypelib">LoadTypeLib</a>, <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-gettypeinfoofguid">GetTypeInfoOfGuid</a>, and <b>CreateStdDispatch</b> comprise the minimum set of functions that you need to call to expose an object using a type library. For more information on <b>LoadTypeLib</b> and <b>GetTypeInfoOfGuid</b>, see <a href="/previous-versions/windows/desktop/automat/type-description-interfaces">Type Description Interfaces</a>. 


<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createdisptypeinfo">CreateDispTypeInfo</a> and <b>CreateStdDispatch</b> comprise the minimum set of dispatch components you need to call to expose an object using type information provided by the INTERFACEDATA structure.


#### Examples

The following code implements the <b>IDispatch</b> interface for the <b>CCalc</b> class using <b>CreateStdDispatch</b>.


```cpp
CCalc FAR*
CCalc::Create()
{
   HRESULT hresult;
   CCalc * pcalc;
   CArith * parith;
   ITypeInfo* ptinfo;
   IUnknown * punkStdDisp;
extern INTERFACEDATA NEARDATA g_idataCCalc;

   if((pcalc = new FAR CCalc()) == NULL)
      return NULL;
   pcalc->AddRef();

   parith = &(pcalc->m_arith);

   // Build type information for the functionality on this object that
   // is being exposed for external programmability.
   hresult = CreateDispTypeInfo(
      &g_idataCCalc, LOCALE_SYSTEM_DEFAULT, &ptinfo);
   if(hresult != NOERROR)
      goto LError0;

   // Create an aggregate with an instance of the default
   // implementation of IDispatch that is initialized with
   // type information.
   hresult = CreateStdDispatch(
      pcalc,            // Controlling unknown.
      parith,            // Instance to dispatch on.
      ptinfo,            // Type information describing the instance.
      &punkStdDisp);

   ptinfo-&>Release();

   if(hresult != NOERROR)
      goto LError0;

   pcalc->m_punkStdDisp = punkStdDisp;

   return pcalc;

LError0:;
   pcalc->Release();
   return NULL;
}
```

## -see-also

<a href="/previous-versions/windows/desktop/automat/dispatch-functions">Creation of Dispatch API Functions</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>