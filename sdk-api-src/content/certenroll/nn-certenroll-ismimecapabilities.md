---
UID: NN:certenroll.ISmimeCapabilities
title: ISmimeCapabilities
author: windows-driver-content
description: Defines the following methods and properties to manage a collection of ISmimeCapability objects.
old-location: security\ismimecapabilities.htm
old-project: SecCertEnroll
ms.assetid: f9750b68-9d35-4594-96fc-2fbd54a87dcc
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: ISmimeCapabilities, ISmimeCapabilities interface [Security], ISmimeCapabilities interface [Security],described, certenroll/ISmimeCapabilities, security.ismimecapabilities
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
-	ISmimeCapabilities
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ISmimeCapabilities interface


## -description


The <b>ISmimeCapabilities</b> interface defines the following methods and properties to manage a collection of <a href="https://msdn.microsoft.com/3cfbb16f-88fa-41f1-b719-cd5e8ad636cc">ISmimeCapability</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISmimeCapabilities</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ISmimeCapabilities</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISmimeCapabilities</b> interface has these methods.
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
Adds an <a href="https://msdn.microsoft.com/3cfbb16f-88fa-41f1-b719-cd5e8ad636cc">ISmimeCapability</a> object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3b087e7-9934-4d29-a516-db5bba824774">AddAvailableSmimeCapabilities</a>
</td>
<td align="left" width="63%">
Adds objects to the collection by identifying the encryption algorithms supported by the default RSA cryptographic provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4244a4e-6ec3-4c1f-a0d6-607cc942b5f5">AddFromCsp</a>
</td>
<td align="left" width="63%">
Adds objects to the collection by identifying the encryption algorithms supported by a specific provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Removes all objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes an object from the collection by index value.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISmimeCapabilities</b> interface has these properties.
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
Retrieves the number of objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fbb51882-4b56-4648-a0ca-0c93311cebbd">ItemByIndex</a>


</td>
<td align="left" width="63%">
Retrieves an object from the collection by index number.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

