---
UID: NN:azroles.IAzClientContext3
title: IAzClientContext3 (azroles.h)
description: Extends the IAzClientContext2 interface.
helpviewer_keywords: ["IAzClientContext3","IAzClientContext3 interface [Security]","IAzClientContext3 interface [Security]","described","azroles/IAzClientContext3","security.iazclientcontext3"]
old-location: security\iazclientcontext3.htm
tech.root: security
ms.assetid: 9435e41b-b2ec-4a2a-9058-82025f2c2e09
ms.date: 12/05/2018
ms.keywords: IAzClientContext3, IAzClientContext3 interface [Security], IAzClientContext3 interface [Security],described, azroles/IAzClientContext3, security.iazclientcontext3
f1_keywords:
- azroles/IAzClientContext3
dev_langs:
- c++
req.header: azroles.h
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
req.dll: Azroles.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Azroles.dll
api_name:
- IAzClientContext3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzClientContext3 interface


## -description


The <b>IAzClientContext3</b> interface extends the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazclientcontext2">IAzClientContext2</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzClientContext3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazclientcontext2">IAzClientContext2</a>. <b>IAzClientContext3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzClientContext3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext3-accesscheck2">AccessCheck2</a>
</td>
<td align="left" width="63%">
Returns a value that specifies whether the principal represented by the current client context is allowed to perform the specified operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext3-getgroups">GetGroups</a>
</td>
<td align="left" width="63%">
Returns an array of the application groups associated with this client context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext3-getoperations">GetOperations</a>
</td>
<td align="left" width="63%">
Returns a collection of the operations, within the specified scope, that the principal represented by the current client context has permission to perform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext3-gettasks">GetTasks</a>
</td>
<td align="left" width="63%">
Returns a collection of the tasks, within the specified scope, that the principal represented by the current client context has permission to perform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext3-isinroleassignment">IsInRoleAssignment</a>
</td>
<td align="left" width="63%">
Checks whether the principal represented by the current client context is a member of the specified role in the specified scope.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzClientContext3</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext3-get_bizruleinterfaces">BizRuleInterfaces</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the collection of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interfaces that can be called by the BizRule script associated with this client context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext3-get_bizruleparameters">BizRuleParameters</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the collection of parameters that can be passed by the BizRule script associated with this client context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext3-get_sids">Sids</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an array of the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs) associated with this client context.

</td>
</tr>
</table> 

