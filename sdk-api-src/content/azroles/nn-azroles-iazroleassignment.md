---
UID: NN:azroles.IAzRoleAssignment
title: IAzRoleAssignment
author: windows-sdk-content
description: Represents a role to which users and groups can be assigned.
old-location: security\iazroleassignment.htm
tech.root: SecAuthZ
ms.assetid: 3f0b926f-77f4-4477-b155-5f866822baba
ms.author: windowssdkdev
ms.date: 10/26/2018
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
 - IAzRoleAssignment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzRoleAssignment interface


## -description


The <b>IAzRoleAssignment</b> interface represents a role to which users and groups can be assigned. A <b>IAzRoleAssignment</b> object can be associated with one or more <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa378367(v=VS.85).aspx">IAzTask</a>, and <a href="https://msdn.microsoft.com/en-us/library/Aa377899(v=VS.85).aspx">IAzOperation</a> objects that specify the operations to which users and groups assigned to the role can access.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzRoleAssignment</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa377917(v=VS.85).aspx">IAzRole</a>. <b>IAzRoleAssignment</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377923(v=VS.85).aspx">AddRoleDefinition</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a> object to this <b>IAzRoleAssignment</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377924(v=VS.85).aspx">DeleteRoleDefinition</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a> object with the specified name from this <b>IAzRoleAssignment</b> object.

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

<a href="https://msdn.microsoft.com/en-us/library/Aa377925(v=VS.85).aspx">RoleDefinitions</a>


</td>
<td align="left" width="63%">
Retrieves a collection of the <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a> objects associated with this <b>IAzRoleAssignment</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377926(v=VS.85).aspx">Scope</a>


</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/en-us/library/Aa378237(v=VS.85).aspx">IAzScope</a> object that represents the scope in which this <b>IAzRoleAssignment</b> object is defined.

</td>
</tr>
</table> 

