---
UID: NN:azroles.IAzRoleAssignment
title: IAzRoleAssignment (azroles.h)
description: Represents a role to which users and groups can be assigned.
helpviewer_keywords: ["IAzRoleAssignment","IAzRoleAssignment interface [Security]","IAzRoleAssignment interface [Security]","described","azroles/IAzRoleAssignment","security.iazroleassignment"]
old-location: security\iazroleassignment.htm
tech.root: security
ms.assetid: 3f0b926f-77f4-4477-b155-5f866822baba
ms.date: 12/05/2018
ms.keywords: IAzRoleAssignment, IAzRoleAssignment interface [Security], IAzRoleAssignment interface [Security],described, azroles/IAzRoleAssignment, security.iazroleassignment
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzRoleAssignment
 - azroles/IAzRoleAssignment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzRoleAssignment
---

# IAzRoleAssignment interface


## -description

The <b>IAzRoleAssignment</b> interface represents a role to which users and groups can be assigned. A <b>IAzRoleAssignment</b> object can be associated with one or more <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a>, <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a>, and <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> objects that specify the operations to which users and groups assigned to the role can access.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzRoleAssignment</b> interface inherits from <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a>. <b>IAzRoleAssignment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzRoleAssignment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazroleassignment-addroledefinition">AddRoleDefinition</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object to this <b>IAzRoleAssignment</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazroleassignment-deleteroledefinition">DeleteRoleDefinition</a>
</td>
<td align="left" width="63%">
Removes the <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object with the specified name from this <b>IAzRoleAssignment</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzRoleAssignment</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazroleassignment-get_roledefinitions">RoleDefinitions</a>


</td>
<td align="left" width="63%">
Retrieves a collection of the <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> objects associated with this <b>IAzRoleAssignment</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazroleassignment-get_scope">Scope</a>


</td>
<td align="left" width="63%">
Retrieves the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object that represents the scope in which this <b>IAzRoleAssignment</b> object is defined.

</td>
</tr>
</table>