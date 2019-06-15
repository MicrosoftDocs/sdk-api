---
UID: NN:azroles.IAzScope2
title: IAzScope2 (azroles.h)
author: windows-sdk-content
description: Extends the IAzScope interface to manage IAzRoleAssignment and IAzRoleDefinition objects.
old-location: security\iazscope2.htm
tech.root: SecAuthZ
ms.assetid: 536c563e-7a6b-480d-9e83-1d7cc90a795d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAzScope2, IAzScope2 interface [Security], IAzScope2 interface [Security],described, azroles/IAzScope2, security.iazscope2
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
 - IAzScope2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzScope2 interface


## -description


The <b>IAzScope2</b> interface extends the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> interface to manage <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> and <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzScope2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a>. <b>IAzScope2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzScope2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazscope2-createroleassignment">CreateRoleAssignment</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object with the specified name in this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazscope2-createroledefinition">CreateRoleDefinition</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object with the specified name in this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazscope2-deleteroleassignment">DeleteRoleAssignment</a>
</td>
<td align="left" width="63%">
Removes the specified <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object from this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazscope2-deleteroledefinition">DeleteRoleDefinition</a>
</td>
<td align="left" width="63%">
Removes the specified <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object from the <b>IAzScope2</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazscope2-openroleassignment">OpenRoleAssignment</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object with the specified name in this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazscope2-openroledefinition">OpenRoleDefinition</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object with the specified name in this scope.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzScope2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazscope2-get_roleassignments">RoleAssignments</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignments">IAzRoleAssignments</a> object that represents the collection of <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> objects associated with this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazscope2-get_roledefinitions">RoleDefinitions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroledefinitions">IAzRoleDefinitions</a> object that represents the collection of <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> objects associated with this scope.

</td>
</tr>
</table> 

