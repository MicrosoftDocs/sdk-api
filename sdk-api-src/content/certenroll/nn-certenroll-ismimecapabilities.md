---
UID: NN:certenroll.ISmimeCapabilities
title: ISmimeCapabilities
author: windows-sdk-content
description: Defines the following methods and properties to manage a collection of ISmimeCapability objects.
old-location: security\ismimecapabilities.htm
old-project: seccertenroll
ms.assetid: f9750b68-9d35-4594-96fc-2fbd54a87dcc
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISmimeCapabilities, ISmimeCapabilities interface [Security], ISmimeCapabilities interface [Security],described, certenroll/ISmimeCapabilities, security.ismimecapabilities
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ISmimeCapabilities
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
<a href="https://msdn.microsoft.com/8ad35758-0dc1-4887-aea7-b8ead537cab2">Add</a>
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
<a href="https://msdn.microsoft.com/8df8eecd-c20f-40f0-a647-23d25ca76ae4">Clear</a>
</td>
<td align="left" width="63%">
Removes all objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/516726cc-f7b9-4813-999f-036694322fe5">Remove</a>
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

<a href="https://msdn.microsoft.com/f43b3aa4-81c5-411c-bd62-77513f9b7f68">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves the enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5e0ee42f-10aa-45d8-b6c0-16ee0149dec6">Count</a>


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
 

 

