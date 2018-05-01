---
UID: NF:oaidl.IEnumVARIANT.Reset
title: IEnumVARIANT::Reset method
author: windows-driver-content
description: Resets the enumeration sequence to the beginning.
old-location: automat\ienumvariant_reset.htm
old-project: automat
ms.assetid: 0c3f0cd7-6bad-4cb7-8b84-d8a212dbadbd
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: IEnumVARIANT, IEnumVARIANT interface [Automation], Reset method, IEnumVARIANT::Reset, Reset method [Automation], Reset method [Automation], IEnumVARIANT interface, Reset,IEnumVARIANT.Reset, _oa96_IEnumVARIANT::Reset, automat.ienumvariant_reset, oaidl/IEnumVARIANT::Reset
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
-	IEnumVARIANT.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumVARIANT::Reset method


## -description


Resets the enumeration sequence to the beginning.




## -parameters






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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
</table>
 




## -remarks



There is no guarantee that exactly the same set of variants will be enumerated the second time as was enumerated the first time. Although an exact duplicate is desirable, the outcome depends on the collection being enumerated. You may find that it is impractical for some collections to maintain this condition (for example, an enumeration of the files in a directory).


#### Examples

The following code implements <b>IEnumVariant::Reset</b>. A complete example implementation of the <b>IEnumVariant</b> interface is available in the COM Fundamentals Lines sample (Enumvar.cpp).

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP
CEnumVariant::Reset()
{
   m_lCurrent = m_lLBound;
   return NOERROR;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>
 

 

