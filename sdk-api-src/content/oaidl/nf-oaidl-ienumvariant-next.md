---
UID: NF:oaidl.IEnumVARIANT.Next
title: IEnumVARIANT::Next
author: windows-sdk-content
description: Retrieves the specified items in the enumeration sequence.
old-location: automat\ienumvariant_next.htm
tech.root: automat
ms.assetid: 691c1624-8d01-41e0-890e-a4782eba1f59
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumVARIANT interface [Automation],Next method, IEnumVARIANT.Next, IEnumVARIANT::Next, Next, Next method [Automation], Next method [Automation],IEnumVARIANT interface, _oa96_IEnumVARIANT::Next, automat.ienumvariant_next, oaidl/IEnumVARIANT::Next
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - IEnumVARIANT.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumVARIANT::Next


## -description


Retrieves the specified items in the enumeration sequence.


## -parameters




### -param celt [in]

The number of elements to be retrieved


### -param rgVar [out]

An array of at least size <i>celt</i> in which the elements are to be returned.


### -param pCeltFetched [out]

The number of elements returned in <i>rgVar</i>, or NULL.


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
The number of elements returned is <i>celt</i>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of elements returned is less than <i>celt</i>.


</td>
</tr>
</table>
 




## -remarks



If fewer than the requested number of elements remain in the sequence, <b>Next</b> returns only the remaining elements. The actual number of elements is returned in <i>pCeltFetched</i>, unless it is null.


#### Examples

The following code implements <b>IEnumVariant::Next</b>. A complete example implementation of the <b>IEnumVariant</b> interface is available in the COM Fundamentals Lines sample (Enumvar.cpp).

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP
CEnumVariant::Next(ULONG cElements, VARIANT * pvar, ULONG * pcElementFetched)
{
   HRESULT hr;
   ULONG l;
   long l1;
   ULONG l2;

   if (pcElementFetched != NULL)
      *pcElementFetched = 0;

   if (pvar == NULL)
      return E_INVALIDARG;

   for (l=0; l&lt;cElements; l++)
      VariantInit(&amp;pvar[l]);

   // Retrieve the next cElements elements.
   // m_lLBound+m_cElements = # of elements in the m_psa collection.

   for (l1=m_lCurrent, l2=0; l1&lt;(long)(m_lLBound+m_cElements) &amp;&amp;
      l2&lt;cElements; l1++, l2++)
   {
      hr = SafeArrayGetElement(m_psa, &amp;l1, &amp;pvar[l2]); 
      if (FAILED(hr))
         goto error; 
   }
   // Set count of elements retrieved.
   if (pcElementFetched != NULL)
      *pcElementFetched = l2;
   m_lCurrent = l1;

   return  (l2 &lt; cElements) ? S_FALSE : NOERROR;

error:
   for (l=0; l&lt;cElements; l++)
      VariantClear(&amp;pvar[l]);
   return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>
 

 

