---
UID: NN:azroles.IAzRoleDefinition
title: IAzRoleDefinition
author: windows-sdk-content
description: Represents one or more IAzRoleDefinition, IAzTask, and IAzOperation objects that specify a set of operations.
old-location: security\iazroledefinition.htm
tech.root: secauthz
ms.assetid: d951f5cc-85da-4898-a70f-9e50ab66ade5
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IAzRoleDefinition, IAzRoleDefinition interface [Security], IAzRoleDefinition interface [Security],described, azroles/IAzRoleDefinition, security.iazroledefinition
ms.prod: windows
ms.technology: windows-sdk
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
 - IAzRoleDefinition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzRoleDefinition interface


## -description


The <b>IAzRoleDefinition</b> interface represents one or more <b>IAzRoleDefinition</b>, <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a>, and <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> objects that specify a set of operations. If an <a href="https://msdn.microsoft.com/en-us/library/Aa377918(v=VS.85).aspx">IAzRoleAssignment</a> object is associated with an <b>IAzRoleDefinition</b> object, users and groups assigned to that <b>IAzRoleAssignment</b> object are allowed to access the operations specified by that <b>IAzRoleDefinition</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzRoleDefinition</b> interface inherits from <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a>. <b>IAzRoleDefinition</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms692124(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377932(v=VS.85).aspx">AddRoleDefinition</a>
</td>
<td align="left" width="63%">
Adds the specified <b>IAzRoleDefinition</b> object to this <b>IAzRoleDefinition</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377933(v=VS.85).aspx">DeleteRoleDefinition</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa377934(v=VS.85).aspx">RoleAssignments</a>


</td>
<td align="left" width="63%">
Retrieves a collection of <a href="https://msdn.microsoft.com/en-us/library/Aa377918(v=VS.85).aspx">IAzRoleAssignment</a> objects that represent the role assignments associated with this <b>IAzRoleDefinition</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377935(v=VS.85).aspx">RoleDefinitions</a>


</td>
<td align="left" width="63%">
Retrieves a collection of the <b>IAzRoleDefinition</b> objects associated with this <b>IAzRoleDefinition</b> object.

</td>
</tr>
</table> 

