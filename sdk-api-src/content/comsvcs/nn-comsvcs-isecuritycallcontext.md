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

# ISecurityCallContext interface


## -description


Provides access to security methods and information about the security call context of the current call. COM+ applications that use role-based security have access to the security call context property collection through this interface. You can obtain information about any caller in the chain of callers, as well as methods specific to COM+ role-based security. For more information, see <a href="https://msdn.microsoft.com/6117970c-5dbd-485e-978e-3aa96e42b359">Programmatic Component Security</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityCallContext</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ISecurityCallContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISecurityCallContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b449a373-2d14-43c5-98b5-ba8119b61e4c">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the security call context collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aebb28de-79ee-4cec-afb9-cfb067a4fb62">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of properties in the security context collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6561b89-8af6-46cc-aeab-2b007d48fe26">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves a specified property in the security call context collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/544deb46-6427-4936-97a6-ea995b5e77ba">IsCallerInRole</a>
</td>
<td align="left" width="63%">
Determines whether the direct caller is in the specified role.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b247d430-56b1-40be-a85a-5ed141d90c85">IsSecurityEnabled</a>
</td>
<td align="left" width="63%">
Determines whether security is enabled for the object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aae5d89a-be46-40c8-ad5d-21f9b3a9c04f">IsUserInRole</a>
</td>
<td align="left" width="63%">
Determines whether the specified user is in the specified role. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b82e32c0-840d-402e-90d5-ff678c51faf1">CoGetCallContext</a>



<a href="https://msdn.microsoft.com/b9b16d2e-92fd-40d2-b33d-8a82a1291794">ISecurityCallersColl</a>



<a href="https://msdn.microsoft.com/6844bfb2-028f-4155-85a6-b7023432f6cd">ISecurityIdentityColl</a>
 

 

