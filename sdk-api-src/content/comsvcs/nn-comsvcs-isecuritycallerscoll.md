---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISecurityCallersColl interface


## -description


Provides access to information about individual callers in a collection of callers. The collection represents the chain of calls ending with the current call, and each caller in the collection represents the identity of one caller. Only callers who cross a boundary where security is checked are included in the chain of callers. (In the COM+ environment, security is checked at application boundaries.) Access to information about a particular caller's identity is provided through <a href="https://msdn.microsoft.com/6844bfb2-028f-4155-85a6-b7023432f6cd">ISecurityIdentityColl</a>, an identity collection. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityCallersColl</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ISecurityCallersColl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISecurityCallersColl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80fb8fe7-0f8f-497c-a046-82f19d6469d8">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the security callers collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98a28194-c4d3-4c5f-b43a-4df73fcea7e4">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of callers in the security callers collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24473ebe-8d29-46cd-817d-48f24b03c405">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves a specified caller in the security callers collection.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b82e32c0-840d-402e-90d5-ff678c51faf1">CoGetCallContext</a>



<a href="https://msdn.microsoft.com/cd96ef31-784f-40fa-beb5-92a88823326b">ISecurityCallContext</a>



<a href="https://msdn.microsoft.com/6844bfb2-028f-4155-85a6-b7023432f6cd">ISecurityIdentityColl</a>



<a href="https://msdn.microsoft.com/164fe12d-eeb3-402f-8aa3-e3545904d9c4">SecurityCallers</a>
 

 

