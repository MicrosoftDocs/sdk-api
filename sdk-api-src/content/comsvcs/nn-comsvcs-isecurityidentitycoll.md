---
UID: NN:comsvcs.ISecurityIdentityColl
title: ISecurityIdentityColl (comsvcs.h)
author: windows-sdk-content
description: Provides access to a collection of security information representing a caller's identity. The items available in this collection are the SID, the account name, the authentication service, the authentication level, and the impersonation level.
old-location: cos\isecurityidentitycoll.htm
tech.root: cossdk
ms.assetid: 6844bfb2-028f-4155-85a6-b7023432f6cd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISecurityIdentityColl, ISecurityIdentityColl interface [COM+], ISecurityIdentityColl interface [COM+],described, _cos_ISecurityIdentityColl, comsvcs/ISecurityIdentityColl, cos.isecurityidentitycoll
ms.topic: interface
f1_keywords: 
 - "comsvcs/ISecurityIdentityColl"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISecurityIdentityColl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISecurityIdentityColl interface


## -description


Provides access to a collection of security information representing a caller's identity. The items available in this collection are the SID, the account name, the authentication service, the authentication level, and the impersonation level.

This interface is used to find out about a particular caller in a chain of callers that is part of the security call context. For more information about how security call context information is accessed, see <a href="https://docs.microsoft.com/windows/desktop/cossdk/programmatic-component-security">Programmatic Component Security</a>. 

COM+ applications that do not use role-based security and base COM applications cannot call methods of <b>ISecurityIdentityColl</b> because they cannot obtain the necessary pointer to <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityIdentityColl</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISecurityIdentityColl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isecurityidentitycoll-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the security identity collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isecurityidentitycoll-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of properties in the security identity collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isecurityidentitycoll-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves a specified property in the security identity collection.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallerscoll">ISecurityCallersColl</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/securityidentity">SecurityIdentity</a>
 

 

