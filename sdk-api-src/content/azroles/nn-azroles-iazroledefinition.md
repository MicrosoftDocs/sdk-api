---
UID: NN:azroles.IAzRoleDefinition
title: IAzRoleDefinition
author: windows-sdk-content
description: Represents one or more IAzRoleDefinition, IAzTask, and IAzOperation objects that specify a set of operations.
old-location: security\iazroledefinition.htm
old-project: SecAuthZ
ms.assetid: d951f5cc-85da-4898-a70f-9e50ab66ade5
ms.author: windowssdkdev
ms.date: 05/22/2018
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzRoleDefinition
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzRoleDefinition interface


## -description


The <b>IAzRoleDefinition</b> interface represents one or more <b>IAzRoleDefinition</b>, <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a>, and <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> objects that specify a set of operations. If an <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object is associated with an <b>IAzRoleDefinition</b> object, users and groups assigned to that <b>IAzRoleAssignment</b> object are allowed to access the operations specified by that <b>IAzRoleDefinition</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzRoleDefinition</b> interface inherits from <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a>. <b>IAzRoleDefinition</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/38d65f5f-452b-4641-a683-2740fb529064">AddRoleDefinition</a>
</td>
<td align="left" width="63%">
Adds the specified <b>IAzRoleDefinition</b> object to this <b>IAzRoleDefinition</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aba2f195-ebd8-40a2-8af4-455144822588">DeleteRoleDefinition</a>
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

<a href="https://msdn.microsoft.com/1b8c3aaf-ed33-4253-b15f-06e5d3415d58">RoleAssignments</a>


</td>
<td align="left" width="63%">
Retrieves a collection of <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> objects that represent the role assignments associated with this <b>IAzRoleDefinition</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/362df9e2-af74-48b7-a6f4-aaa6ad1d8df5">RoleDefinitions</a>


</td>
<td align="left" width="63%">
Retrieves a collection of the <b>IAzRoleDefinition</b> objects associated with this <b>IAzRoleDefinition</b> object.

</td>
</tr>
</table> 

