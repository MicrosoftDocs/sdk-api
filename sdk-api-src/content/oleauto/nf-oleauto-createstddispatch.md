---
UID: NF:oleauto.CreateStdDispatch
title: CreateStdDispatch function
author: windows-sdk-content
description: Creates a standard implementation of the IDispatch interface through a single function call. This simplifies exposing objects through Automation.
old-location: automat\createstddispatch.htm
old-project: automat
ms.assetid: 45a59243-df93-41ca-ac60-354cb1165004
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: CreateStdDispatch, CreateStdDispatch function [Automation], _oa96_CreateStdDispatch, automat.createstddispatch, oleauto/CreateStdDispatch
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: REGKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	CreateStdDispatch
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CreateStdDispatch function


## -description


Creates a standard implementation of the <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface through a single function call. This simplifies exposing objects through Automation.


## -parameters




### -param punkOuter

The object's <b>IUnknown</b> implementation.




### -param pvThis

The object to expose.


### -param ptinfo

The type information that describes the exposed object.



### -param ppunkStdDisp

The private unknown for the object that implements the <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface QueryInterface call. This pointer is null if the function fails.


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



You can use <b>CreateStdDispatch</b> when creating an object instead of implementing the <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> member functions for the object. However, the implementation that <b>CreateStdDispatch</b> creates has these limitations:  

<ul>
<li>
Supports only one national language.

</li>
<li>
Supports only dispatch-defined exception codes returned from <a href="https://msdn.microsoft.com/964ade8e-9d8a-4d32-bd47-aa678912a54d">Invoke</a>.

</li>
</ul>

<a href="https://msdn.microsoft.com/155b48e5-5438-409e-9342-630a6a500f60">LoadTypeLib</a>, <a href="https://msdn.microsoft.com/58f96322-f1cd-448c-906d-b7faa65ab9a0">GetTypeInfoOfGuid</a>, and <b>CreateStdDispatch</b> comprise the minimum set of functions that you need to call to expose an object using a type library. For more information on <b>LoadTypeLib</b> and <b>GetTypeInfoOfGuid</b>, see <a href="https://msdn.microsoft.com/ab44422c-97d6-4a63-ade1-db919d53aae7">Type Description Interfaces</a>. 


<a href="https://msdn.microsoft.com/603e00e8-0370-4ebf-b9d2-85e6e58c2b3a">CreateDispTypeInfo</a> and <b>CreateStdDispatch</b> comprise the minimum set of dispatch components you need to call to expose an object using type information provided by the INTERFACEDATA structure.


#### Examples

The following code implements the <b>IDispatch</b> interface for the <b>CCalc</b> class using <b>CreateStdDispatch</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CCalc FAR*
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
   pcalc-&gt;AddRef();

   parith = &amp;(pcalc-&gt;m_arith);

   // Build type information for the functionality on this object that
   // is being exposed for external programmability.
   hresult = CreateDispTypeInfo(
      &amp;g_idataCCalc, LOCALE_SYSTEM_DEFAULT, &amp;ptinfo);
   if(hresult != NOERROR)
      goto LError0;

   // Create an aggregate with an instance of the default
   // implementation of IDispatch that is initialized with
   // type information.
   hresult = CreateStdDispatch(
      pcalc,            // Controlling unknown.
      parith,            // Instance to dispatch on.
      ptinfo,            // Type information describing the instance.
      &amp;punkStdDisp);

   ptinfo-&amp;&gt;Release();

   if(hresult != NOERROR)
      goto LError0;

   pcalc-&gt;m_punkStdDisp = punkStdDisp;

   return pcalc;

LError0:;
   pcalc-&gt;Release();
   return NULL;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2c66b04e-9d96-45e9-8105-82d58a5a4085">Creation of Dispatch API Functions</a>



<a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

