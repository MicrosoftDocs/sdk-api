---
UID: NN:comsvcs.ISecurityIdentityColl
title: ISecurityIdentityColl
author: windows-sdk-content
description: Provides access to a collection of security information representing a caller's identity. The items available in this collection are the SID, the account name, the authentication service, the authentication level, and the impersonation level.
old-location: cos\isecurityidentitycoll.htm
old-project: cossdk
ms.assetid: 6844bfb2-028f-4155-85a6-b7023432f6cd
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: ISecurityIdentityColl, ISecurityIdentityColl interface [COM+], ISecurityIdentityColl interface [COM+],described, _cos_ISecurityIdentityColl, comsvcs/ISecurityIdentityColl, cos.isecurityidentitycoll
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISecurityIdentityColl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISecurityIdentityColl interface


## -description


Provides access to a collection of security information representing a caller's identity. The items available in this collection are the SID, the account name, the authentication service, the authentication level, and the impersonation level.

This interface is used to find out about a particular caller in a chain of callers that is part of the security call context. For more information about how security call context information is accessed, see <a href="https://msdn.microsoft.com/6117970c-5dbd-485e-978e-3aa96e42b359">Programmatic Component Security</a>. 

COM+ applications that do not use role-based security and base COM applications cannot call methods of <b>ISecurityIdentityColl</b> because they cannot obtain the necessary pointer to <a href="https://msdn.microsoft.com/cd96ef31-784f-40fa-beb5-92a88823326b">ISecurityCallContext</a>. For more information, see <a href="https://msdn.microsoft.com/b82e32c0-840d-402e-90d5-ff678c51faf1">CoGetCallContext</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityIdentityColl</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ISecurityIdentityColl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISecurityIdentityColl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e138b0b-cea1-47ca-a73b-473b9f5860db">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the security identity collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43363504-ee5e-4d1c-a7eb-c4f003d84d57">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of properties in the security identity collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0cc3a905-ec06-4d8d-8e4a-0774b7e67282">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves a specified property in the security identity collection.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b82e32c0-840d-402e-90d5-ff678c51faf1">CoGetCallContext</a>



<a href="https://msdn.microsoft.com/b9b16d2e-92fd-40d2-b33d-8a82a1291794">ISecurityCallersColl</a>



<a href="https://msdn.microsoft.com/c6b28695-1b08-490a-8d56-eb55d82f3e7a">SecurityIdentity</a>
 

 

