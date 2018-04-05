---
UID: NF:oaidl.IEnumVARIANT.Clone
title: IEnumVARIANT::Clone method
author: windows-driver-content
description: Creates a copy of the current state of enumeration.
old-location: automat\ienumvariant_clone.htm
old-project: automat
ms.assetid: 44beac4a-784d-461e-8a4b-71bdcf512fbc
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: Clone method [Automation], Clone method [Automation], IEnumVARIANT interface, Clone,IEnumVARIANT.Clone, IEnumVARIANT, IEnumVARIANT interface [Automation], Clone method, IEnumVARIANT::Clone, _oa96_IEnumVARIANT::Clone, automat.ienumvariant_clone, oaidl/IEnumVARIANT::Clone
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
req.typenames: VARKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	oaidl.h
api_name:
-	IEnumVARIANT.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IEnumVARIANT::Clone method


## -description


Creates a copy of the current state of enumeration.




## -parameters




### -param ppEnum [out]

The clone enumerator.


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



Using this function, a particular point in the enumeration sequence can be recorded, and then returned to at a later time. The returned enumerator is of the same actual interface as the one that is being cloned.

There is no guarantee that exactly the same set of variants will be enumerated the second time as was enumerated the first. Although an exact duplicate is desirable, the outcome depends on the collection being enumerated. You may find that it is impractical for some collections to maintain this condition (for example, an enumeration of the files in a directory).


#### Examples

The following code implements <b>IEnumVariant::Clone</b>. A complete example implementation of the <b>IEnumVariant</b> interface is available in the COM Fundamentals Lines sample (Enumvar.cpp).

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP
CEnumVariant::Clone(IEnumVARIANT ** ppenum)
{
   CEnumVariant * penum = NULL;
   HRESULT hr;

   if (ppenum == NULL)
      return E_INVALIDARG;

   *ppenum = NULL;

   hr = CEnumVariant::Create(m_psa, m_cElements, &amp;penum);
   if (FAILED(hr))
      goto error;
   penum-&gt;AddRef();
   penum-&gt;m_lCurrent = m_lCurrent;

   *ppenum = penum;
   return NOERROR;

error:
   if (penum)
      penum-&gt;Release();
   return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>
 

 

