---
UID: NN:certenroll.ICryptAttributes
title: ICryptAttributes
author: windows-driver-content
description: The ICryptAttributes interface contains methods and properties that enable you to manage a collection of ICryptAttribute objects.
old-location: security\icryptattributes.htm
old-project: SecCertEnroll
ms.assetid: beedb57c-1c89-4d16-8514-046e3071fd1e
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ICryptAttributes, ICryptAttributes interface [Security], ICryptAttributes interface [Security], described, certenroll/ICryptAttributes, security.icryptattributes
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
-	ICryptAttributes
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICryptAttributes interface


## -description


The <b>ICryptAttributes</b> interface contains methods and properties that enable you to manage a collection of <a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICryptAttributes</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICryptAttributes</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICryptAttributes</b> interface has these methods.
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
Adds an <a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a> object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8dc0a2c5-3734-47c7-a716-f53322fee39d">AddRange</a>
</td>
<td align="left" width="63%">
Adds a range of <a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a> objects to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Removes all <a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a> objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes an <a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a> object from the collection by index number.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICryptAttributes</b> interface has these properties.
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
Retrieves the number of <a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a> objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e294e205-791f-444e-92d8-78da347616a7">IndexByObjectId</a>


</td>
<td align="left" width="63%">
Retrieves the index of an attribute by object identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/327a41ee-60ed-44a0-bfd8-96b328b4fcb6">ItemByIndex</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a> object from the collection by index number.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

