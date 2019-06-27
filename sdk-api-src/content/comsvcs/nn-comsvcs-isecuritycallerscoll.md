---
UID: NN:comsvcs.ISecurityCallersColl
title: ISecurityCallersColl (comsvcs.h)
author: windows-sdk-content
description: Provides access to information about individual callers in a collection of callers.
old-location: cos\isecuritycallerscoll.htm
tech.root: cossdk
ms.assetid: b9b16d2e-92fd-40d2-b33d-8a82a1291794
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISecurityCallersColl, ISecurityCallersColl interface [COM+], ISecurityCallersColl interface [COM+],described, _cos_ISecurityCallersColl, comsvcs/ISecurityCallersColl, cos.isecuritycallerscoll
ms.topic: interface
f1_keywords: 
 - "comsvcs/ISecurityCallersColl"
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
 - ISecurityCallersColl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISecurityCallersColl interface


## -description


Provides access to information about individual callers in a collection of callers. The collection represents the chain of calls ending with the current call, and each caller in the collection represents the identity of one caller. Only callers who cross a boundary where security is checked are included in the chain of callers. (In the COM+ environment, security is checked at application boundaries.) Access to information about a particular caller's identity is provided through <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-isecurityidentitycoll">ISecurityIdentityColl</a>, an identity collection. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityCallersColl</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISecurityCallersColl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isecuritycallerscoll-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the security callers collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isecuritycallerscoll-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of callers in the security callers collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isecuritycallerscoll-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves a specified caller in the security callers collection.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-isecurityidentitycoll">ISecurityIdentityColl</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/securitycallers">SecurityCallers</a>
 

 

