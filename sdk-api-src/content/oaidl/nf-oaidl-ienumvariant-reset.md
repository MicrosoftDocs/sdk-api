---
UID: NF:oaidl.IEnumVARIANT.Reset
title: IEnumVARIANT::Reset (oaidl.h)
author: windows-sdk-content
description: Resets the enumeration sequence to the beginning.
old-location: automat\ienumvariant_reset.htm
tech.root: automat
ms.assetid: 0c3f0cd7-6bad-4cb7-8b84-d8a212dbadbd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumVARIANT interface [Automation],Reset method, IEnumVARIANT.Reset, IEnumVARIANT::Reset, Reset, Reset method [Automation], Reset method [Automation],IEnumVARIANT interface, _oa96_IEnumVARIANT::Reset, automat.ienumvariant_reset, oaidl/IEnumVARIANT::Reset
ms.topic: method
f1_keywords: 
 - "oaidl/IEnumVARIANT.Reset"
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
 - IEnumVARIANT.Reset
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumVARIANT::Reset


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


```cpp
STDMETHODIMP
CEnumVariant::Reset()
{
   m_lCurrent = m_lLBound;
   return NOERROR;
}
```





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>
 

 

