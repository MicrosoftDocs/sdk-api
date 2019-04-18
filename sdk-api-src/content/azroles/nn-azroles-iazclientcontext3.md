---
UID: NN:azroles.IAzClientContext3
title: IAzClientContext3 (azroles.h)
author: windows-sdk-content
description: Extends the IAzClientContext2 interface.
old-location: security\iazclientcontext3.htm
tech.root: SecAuthZ
ms.assetid: 9435e41b-b2ec-4a2a-9058-82025f2c2e09
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAzClientContext3, IAzClientContext3 interface [Security], IAzClientContext3 interface [Security],described, azroles/IAzClientContext3, security.iazclientcontext3
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzClientContext3 interface


## -description


The <b>IAzClientContext3</b> interface extends the <a href="https://msdn.microsoft.com/8e922370-18e3-481c-93f2-9a56d7898ba7">IAzClientContext2</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzClientContext3</b> interface inherits from <a href="https://msdn.microsoft.com/8e922370-18e3-481c-93f2-9a56d7898ba7">IAzClientContext2</a>. <b>IAzClientContext3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/042d1f51-5eb8-4c32-97f1-bb76546e6624">AccessCheck2</a>
</td>
<td align="left" width="63%">
Returns a value that specifies whether the principal represented by the current client context is allowed to perform the specified operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e34b55e1-df7f-4356-b84e-8f297afcda24">GetGroups</a>
</td>
<td align="left" width="63%">
Returns an array of the application groups associated with this client context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f5c7e2d-e88d-4236-888c-9bf5a425713c">GetOperations</a>
</td>
<td align="left" width="63%">
Returns a collection of the operations, within the specified scope, that the principal represented by the current client context has permission to perform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/285f0e9a-8604-4475-8a73-ed33581f87f4">GetTasks</a>
</td>
<td align="left" width="63%">
Returns a collection of the tasks, within the specified scope, that the principal represented by the current client context has permission to perform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20e19ee7-3b65-4f0f-ba19-7fb6cbbaea7b">IsInRoleAssignment</a>
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

<a href="https://msdn.microsoft.com/6cb1e53e-2e15-4f5f-9a8e-e9f988370cba">BizRuleInterfaces</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the collection of <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interfaces that can be called by the BizRule script associated with this client context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/161f8a84-ee00-4f39-9997-a1e3d1c5b7a8">BizRuleParameters</a>


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

<a href="https://msdn.microsoft.com/79caf62e-3f20-4a58-953f-c9d302208bf9">Sids</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an array of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs) associated with this client context.

</td>
</tr>
</table> 

