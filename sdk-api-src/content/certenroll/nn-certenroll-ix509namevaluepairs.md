---
UID: NN:certenroll.IX509NameValuePairs
title: IX509NameValuePairs
author: windows-driver-content
description: The IX509NameValuePairs interface defines the following methods and properties to manage a collection of IX509NameValuePair objects.
old-location: security\ix509namevaluepairs.htm
old-project: SecCertEnroll
ms.assetid: c881dc9f-4187-4ba1-9f3a-e1564e4f37c7
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IX509NameValuePairs, IX509NameValuePairs interface [Security], IX509NameValuePairs interface [Security],described, certenroll/IX509NameValuePairs, security.ix509namevaluepairs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509NameValuePairs
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509NameValuePairs interface


## -description


The <b>IX509NameValuePairs</b> interface defines the following methods and properties to manage a collection of <a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">IX509NameValuePair</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509NameValuePairs</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IX509NameValuePairs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509NameValuePairs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">IX509NameValuePair</a> object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Removes all <a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">IX509NameValuePair</a> objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes an <a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">IX509NameValuePair</a> object from the collection by index number.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509NameValuePairs</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves the enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of <a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">IX509NameValuePair</a> objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/76c00e96-e563-45e1-a579-9efafbc227b2">ItemByIndex</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">IX509NameValuePair</a> object from the collection by index number.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">IX509NameValuePair</a>
 

 

