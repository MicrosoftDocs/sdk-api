---
UID: NN:azroles.IAzApplication3
title: IAzApplication3
author: windows-sdk-content
description: Provides methods to manage IAzRoleAssignment, IAzRoleDefinition, and IAzScope2 objects.
old-location: security\iazapplication3.htm
tech.root: SecAuthZ
ms.assetid: 9d0b2c3b-b8b6-4fae-9308-9dd29da0724f
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: IAzApplication3, IAzApplication3 interface [Security], IAzApplication3 interface [Security],described, azroles/IAzApplication3, security.iazapplication3
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
 - IAzApplication3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzApplication3 interface


## -description


The <b>IAzApplication3</b> interface provides methods to manage <a href="https://msdn.microsoft.com/en-us/library/Aa377918(v=VS.85).aspx">IAzRoleAssignment</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a>, and <a href="https://msdn.microsoft.com/en-us/library/Aa378239(v=VS.85).aspx">IAzScope2</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplication3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa446685(v=VS.85).aspx">IAzApplication2</a>. <b>IAzApplication3</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>IAzApplication3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa446689(v=VS.85).aspx">CreateRoleAssignment</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/en-us/library/Aa377918(v=VS.85).aspx">IAzRoleAssignment</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa446690(v=VS.85).aspx">CreateRoleDefinition</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376903(v=VS.85).aspx">CreateScope2</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/en-us/library/Aa378239(v=VS.85).aspx">IAzScope2</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377009(v=VS.85).aspx">DeleteRoleAssignment</a>
</td>
<td align="left" width="63%">
Removes the specified <a href="https://msdn.microsoft.com/en-us/library/Aa377918(v=VS.85).aspx">IAzRoleAssignment</a> object from the <b>IAzApplication3</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377016(v=VS.85).aspx">DeleteRoleDefinition</a>
</td>
<td align="left" width="63%">
Removes the specified <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a> object from the <b>IAzApplication3</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377025(v=VS.85).aspx">DeleteScope2</a>
</td>
<td align="left" width="63%">
Removes the specified <a href="https://msdn.microsoft.com/en-us/library/Aa378239(v=VS.85).aspx">IAzScope2</a> object from the <b>IAzApplication3</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377030(v=VS.85).aspx">OpenRoleAssignment</a>
</td>
<td align="left" width="63%">
Opens the specified <a href="https://msdn.microsoft.com/en-us/library/Aa377918(v=VS.85).aspx">IAzRoleAssignment</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377036(v=VS.85).aspx">OpenRoleDefinition</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377137(v=VS.85).aspx">OpenScope2</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/en-us/library/Aa378239(v=VS.85).aspx">IAzScope2</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377248(v=VS.85).aspx">ScopeExists</a>
</td>
<td align="left" width="63%">
Indicates whether the scope with the specified name exists in the <b>IAzApplication3</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplication3</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Ff717851(v=VS.85).aspx">BizRulesEnabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that indicates whether business rules are enabled for the current <b>IAzApplication3</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377239(v=VS.85).aspx">RoleAssignments</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/en-us/library/Aa377919(v=VS.85).aspx">IAzRoleAssignments</a> object that represents the collection of <a href="https://msdn.microsoft.com/en-us/library/Aa377918(v=VS.85).aspx">IAzRoleAssignment</a> objects associated with the current <b>IAzApplication3</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377245(v=VS.85).aspx">RoleDefinitions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/en-us/library/Aa377928(v=VS.85).aspx">IAzRoleDefinitions</a> object that represents the collection of <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a> objects associated with the current <b>IAzApplication3</b> object.

</td>
</tr>
</table> 

