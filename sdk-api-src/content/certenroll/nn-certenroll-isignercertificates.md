---
UID: NN:certenroll.ISignerCertificates
title: ISignerCertificates
author: windows-sdk-content
description: The ISignerCertificates interface defines the following methods and properties to manage a collection of ISignerCertificate objects.
old-location: security\isignercertificates.htm
old-project: SecCertEnroll
ms.assetid: 420d6550-514a-4fea-987b-6deecbc9b717
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ISignerCertificates, ISignerCertificates interface [Security], ISignerCertificates interface [Security],described, certenroll/ISignerCertificates, security.isignercertificates
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	ISignerCertificates
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ISignerCertificates interface


## -description


The <b>ISignerCertificates</b> interface defines the following methods and properties to manage a collection of <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISignerCertificates</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ISignerCertificates</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISignerCertificates</b> interface has these methods.
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
Adds an <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Removes all <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee741eda-e125-4938-bc49-d8089f7d5df2">Find</a>
</td>
<td align="left" width="63%">
Retrieves the index number of an <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes an <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> object from the collection by index number.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISignerCertificates</b> interface has these properties.
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
Retrieves the number of <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/44f9ff7d-5ed2-4575-a9c2-50096fffcf07">ItemByIndex</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> object from the collection by index number.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ae6ab5fc-598e-43b8-a260-2cd94dc2648f">Certificate Enrollment API</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a>
 

 

