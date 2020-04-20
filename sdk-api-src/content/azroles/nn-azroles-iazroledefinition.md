---
UID: NN:azroles.IAzRoleDefinition
title: IAzRoleDefinition (azroles.h)
description: Represents one or more IAzRoleDefinition, IAzTask, and IAzOperation objects that specify a set of operations.helpviewer_keywords: ["IAzRoleDefinition","IAzRoleDefinition interface [Security]","IAzRoleDefinition interface [Security]","described","azroles/IAzRoleDefinition","security.iazroledefinition"]
old-location: security\iazroledefinition.htm
tech.root: SecAuthZ
ms.assetid: d951f5cc-85da-4898-a70f-9e50ab66ade5
ms.date: 12/05/2018
ms.keywords: IAzRoleDefinition, IAzRoleDefinition interface [Security], IAzRoleDefinition interface [Security],described, azroles/IAzRoleDefinition, security.iazroledefinition
f1_keywords:
- azroles/IAzRoleDefinition
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
- IAzRoleDefinition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzRoleDefinition interface


## -description


The <b>IAzRoleDefinition</b> interface represents one or more <b>IAzRoleDefinition</b>, <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> objects that specify a set of operations. If an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object is associated with an <b>IAzRoleDefinition</b> object, users and groups assigned to that <b>IAzRoleAssignment</b> object are allowed to access the operations specified by that <b>IAzRoleDefinition</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzRoleDefinition</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a>. <b>IAzRoleDefinition</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzRoleDefinition</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazroledefinition-addroledefinition">AddRoleDefinition</a>
</td>
<td align="left" width="63%">
Adds the specified <b>IAzRoleDefinition</b> object to this <b>IAzRoleDefinition</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazroledefinition-deleteroledefinition">DeleteRoleDefinition</a>
</td>
<td align="left" width="63%">
Removes the <b>IAzRoleDefinition</b> object with the specified name from this <b>IAzRoleDefinition</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzRoleDefinition</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazroledefinition-roleassignments">RoleAssignments</a>


</td>
<td align="left" width="63%">
Retrieves a collection of <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> objects that represent the role assignments associated with this <b>IAzRoleDefinition</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazroledefinition-get_roledefinitions">RoleDefinitions</a>


</td>
<td align="left" width="63%">
Retrieves a collection of the <b>IAzRoleDefinition</b> objects associated with this <b>IAzRoleDefinition</b> object.

</td>
</tr>
</table> 

