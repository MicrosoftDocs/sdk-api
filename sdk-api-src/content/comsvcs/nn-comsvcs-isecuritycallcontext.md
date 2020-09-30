---
UID: NN:comsvcs.ISecurityCallContext
title: ISecurityCallContext (comsvcs.h)
description: Provides access to security methods and information about the security call context of the current call.
helpviewer_keywords: ["ISecurityCallContext","ISecurityCallContext interface [COM+]","ISecurityCallContext interface [COM+]","described","_cos_ISecurityCallContext","comsvcs/ISecurityCallContext","cos.isecuritycallcontext"]
old-location: cos\isecuritycallcontext.htm
tech.root: cos
ms.assetid: cd96ef31-784f-40fa-beb5-92a88823326b
ms.date: 12/05/2018
ms.keywords: ISecurityCallContext, ISecurityCallContext interface [COM+], ISecurityCallContext interface [COM+],described, _cos_ISecurityCallContext, comsvcs/ISecurityCallContext, cos.isecuritycallcontext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISecurityCallContext
 - comsvcs/ISecurityCallContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISecurityCallContext
---

# ISecurityCallContext interface


## -description

Provides access to security methods and information about the security call context of the current call. COM+ applications that use role-based security have access to the security call context property collection through this interface. You can obtain information about any caller in the chain of callers, as well as methods specific to COM+ role-based security. For more information, see <a href="/windows/desktop/cossdk/programmatic-component-security">Programmatic Component Security</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityCallContext</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISecurityCallContext</b> also has these types of members:
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
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecuritycallcontext-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the security call context collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecuritycallcontext-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of properties in the security context collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecuritycallcontext-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves a specified property in the security call context collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole">IsCallerInRole</a>
</td>
<td align="left" width="63%">
Determines whether the direct caller is in the specified role.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled">IsSecurityEnabled</a>
</td>
<td align="left" width="63%">
Determines whether security is enabled for the object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecuritycallcontext-isuserinrole">IsUserInRole</a>
</td>
<td align="left" width="63%">
Determines whether the specified user is in the specified role. 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallerscoll">ISecurityCallersColl</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecurityidentitycoll">ISecurityIdentityColl</a>