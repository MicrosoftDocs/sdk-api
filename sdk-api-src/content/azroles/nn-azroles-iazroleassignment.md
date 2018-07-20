---
UID: NN:azroles.IAzRoleAssignment
title: IAzRoleAssignment
author: windows-sdk-content
description: Represents a role to which users and groups can be assigned.
old-location: security\iazroleassignment.htm
old-project: SecAuthZ
ms.assetid: 3f0b926f-77f4-4477-b155-5f866822baba
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IAzRoleAssignment, IAzRoleAssignment interface [Security], IAzRoleAssignment interface [Security],described, azroles/IAzRoleAssignment, security.iazroleassignment
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzRoleAssignment
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzRoleAssignment interface


## -description


The <b>IAzRoleAssignment</b> interface represents a role to which users and groups can be assigned. A <b>IAzRoleAssignment</b> object can be associated with one or more <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a>, <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a>, and <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> objects that specify the operations to which users and groups assigned to the role can access.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzRoleAssignment</b> interface inherits from <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a>. <b>IAzRoleAssignment</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/9946d273-3726-40f4-b438-7f2377fc8013">AddRoleDefinition</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object to this <b>IAzRoleAssignment</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17af80d0-d9b4-4e20-b7a8-72e8dc42b69d">DeleteRoleDefinition</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object with the specified name from this <b>IAzRoleAssignment</b> object.

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

<a href="https://msdn.microsoft.com/7528c9aa-264c-4bdc-8a50-c3d41ac00cc5">RoleDefinitions</a>


</td>
<td align="left" width="63%">
Retrieves a collection of the <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> objects associated with this <b>IAzRoleAssignment</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915814">Scope</a>


</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object that represents the scope in which this <b>IAzRoleAssignment</b> object is defined.

</td>
</tr>
</table> 

