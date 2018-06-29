---
UID: NF:oleauto.SafeArrayGetElement
title: SafeArrayGetElement function
author: windows-sdk-content
description: Retrieves a single element of the array.
old-location: automat\safearraygetelement.htm
old-project: automat
ms.assetid: 47e9ee31-1e3b-4193-8467-6ef0db05966e
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: SafeArrayGetElement, SafeArrayGetElement function [Automation], _oa96_SafeArrayGetElement, automat.safearraygetelement, oleauto/SafeArrayGetElement
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
tech.root: 
req.typenames: REGKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayGetElement
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# SafeArrayGetElement function


## -description


Retrieves a single element of the array.


## -parameters




### -param psa [in]

An array descriptor created by <a href="https://msdn.microsoft.com/5b94f1a2-a558-473f-85dd-9545c0464cc7">SafeArrayCreate</a>.



### -param rgIndices [in]

A vector of indexes for each dimension of the array. The right-most (least significant) dimension is rgIndices[0]. The left-most dimension is stored at <code>rgIndices[psa-&gt;cDims – 1]</code>.



### -param pv [out]

The element of the array.


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
<dt><b>DISP_E_BADINDEX</b></dt>
</dl>
</td>
<td width="60%">
The specified index is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory could not be allocated for the element.

</td>
</tr>
</table>
 




## -remarks



This function calls <a href="https://msdn.microsoft.com/cb29d862-c7c5-4852-b017-c29e88d5f1c4">SafeArrayLock</a> and <a href="https://msdn.microsoft.com/654995ab-1959-44dc-9e26-11c34e489c14">SafeArrayUnlock</a> automatically, before and after retrieving the element. The caller must provide a storage area of the correct size to receive the data. If the data element is a string, object, or variant, the function copies the element in the correct way.


#### Examples

The following example is taken from the COM Fundamentals SPoly sample (Cenumpt.cpp).

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CEnumPoint::Next(
   ULONG celt,
   VARIANT  rgvar[],
   ULONG * pceltFetched)
{
   unsigned int i;
   long ix;
   HRESULT hresult;

   for(i = 0; i &lt; celt; ++i)
      VariantInit(&amp;rgvar[i]);

   for(i = 0; i &lt; celt; ++i){
      // Are we at the last element?
      if(m_iCurrent == m_celts){
      hresult = S_FALSE;
         goto LDone;
   }

      ix = m_iCurrent++;
      // m_psa is a global variable that holds the safe array.
      hresult = SafeArrayGetElement(m_psa, &amp;ix, &amp;rgvar[i]);
      if(FAILED(hresult))
         goto LError0;
   }
   hresult = NOERROR;

LDone:;
   if (pceltFetched != NULL)
      *pceltFetched = i;

   return hresult;

LError0:;
   for(i = 0; i &lt; celt; ++i)
      VariantClear(&amp;rgvar[i]);
   return hresult;
}</pre>
</td>
</tr>
</table></span></div>


