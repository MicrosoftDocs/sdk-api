---
UID: NN:certenroll.ICertificatePolicies
title: ICertificatePolicies
author: windows-sdk-content
description: Contains methods and properties that enable you to manage a collection of ICertificatePolicy objects.
old-location: security\icertificatepolicies.htm
tech.root: SecCertEnroll
ms.assetid: 2503adcb-0b73-42ef-98cf-a2b906e34ef7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICertificatePolicies, ICertificatePolicies interface [Security], ICertificatePolicies interface [Security],described, certenroll/ICertificatePolicies, security.icertificatepolicies
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICertificatePolicies
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertificatePolicies interface


## -description


The <b>ICertificatePolicies</b> interface contains methods and properties that enable you to manage a collection of <a href="https://msdn.microsoft.com/2162de70-edcc-4f01-807d-79ff200d0016">ICertificatePolicy</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificatePolicies</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICertificatePolicies</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertificatePolicies</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85dc750c-ef18-4136-962e-c95bcca05b9a">Add</a>
</td>
<td align="left" width="63%">
Adds an object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/842c06a7-bf70-45e5-8f65-edaa075a8f3e">Clear</a>
</td>
<td align="left" width="63%">
Removes all objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cd010bb-50ee-4251-815e-1fb4de1f2a81">Remove</a>
</td>
<td align="left" width="63%">
Removes an object from the collection by index number.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificatePolicies</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/99ce5d45-c2ff-45be-8eb4-e1a57bbfa2fc">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves the enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/292c37c1-8b85-4fa3-8ed8-1728ebe3d177">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dac1a656-265c-41ec-b460-0414fefe3c40">ItemByIndex</a>


</td>
<td align="left" width="63%">
Retrieves an object from the collection by index number.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/2162de70-edcc-4f01-807d-79ff200d0016">ICertificatePolicy</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

