---
UID: NF:oaidl.IDispatch.GetTypeInfoCount
title: IDispatch::GetTypeInfoCount
author: windows-sdk-content
description: Retrieves the number of type information interfaces that an object provides (either 0 or 1).
old-location: automat\idispatch_gettypeinfocount.htm
old-project: automat
ms.assetid: da876d53-cb8a-465c-a43e-c0eb272e2a12
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: GetTypeInfoCount, GetTypeInfoCount method [Automation], GetTypeInfoCount method [Automation],IAccessible interface, GetTypeInfoCount method [Automation],IDispatch interface, IAccessible interface [Automation],GetTypeInfoCount method, IAccessible::GetTypeInfoCount, IDispatch interface [Automation],GetTypeInfoCount method, IDispatch.GetTypeInfoCount, IDispatch::GetTypeInfoCount, _oa96_IDispatch::GetTypeInfoCount, automat.idispatch_gettypeinfocount, oaidl/IAccessible::GetTypeInfoCount, oaidl/IDispatch::GetTypeInfoCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: VARKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	oaidl.h
api_name:
-	IDispatch.GetTypeInfoCount
-	IAccessible.GetTypeInfoCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP
CLines::GetTypeInfoCount(UINT * pctinfo)
{
   if (pctinfo == NULL) {
      return E_INVALIDARG;
}
   *pctinfo = 1;
   return NOERROR;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>



<a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

