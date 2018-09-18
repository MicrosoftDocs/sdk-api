---
UID: NN:azroles.IAzRole
title: IAzRole
author: windows-sdk-content
description: Defines the set of operations that can be performed by a set of users within a scope.
old-location: security\iazrole.htm
tech.root: secauthz
ms.assetid: 2934d783-b379-486c-80e7-e7650b89dc1a
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IAzRole, IAzRole interface [Security], IAzRole interface [Security],described, azroles/IAzRole, security.iazrole
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
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
 - IAzRole
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzRole interface


## -description


The <b>IAzRole</b> interface defines the set of operations that can be performed by a set of users within a scope.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzRole</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAzRole</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzRole</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/118387f8-a422-4a8d-9d12-a5b5ee1e7b06">AddAppMember</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object to the list of application groups that belong to this role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2be62cb-7256-4031-8af9-24f3043a8430">AddMember</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">security identifier</a> (SID) in text form to the list of Windows  accounts that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378163(v=VS.85).aspx">AddMemberName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of  accounts that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378165(v=VS.85).aspx">AddOperation</a>
</td>
<td align="left" width="63%">
Adds the <a href="https://msdn.microsoft.com/en-us/library/Aa377899(v=VS.85).aspx">IAzOperation</a> object with the specified name to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378168(v=VS.85).aspx">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified entity to the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378172(v=VS.85).aspx">AddTask</a>
</td>
<td align="left" width="63%">
Adds the <a href="https://msdn.microsoft.com/en-us/library/Aa378367(v=VS.85).aspx">IAzTask</a> object with the specified name to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378178(v=VS.85).aspx">DeleteAppMember</a>
</td>
<td align="left" width="63%">
Removes the specified <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object from the list of application groups that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378180(v=VS.85).aspx">DeleteMember</a>
</td>
<td align="left" width="63%">
Removes  the specified SID in text form from the list of Windows  accounts that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378182(v=VS.85).aspx">DeleteMemberName</a>
</td>
<td align="left" width="63%">
Removes  the specified account name from the list of accounts that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378183(v=VS.85).aspx">DeleteOperation</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/en-us/library/Aa377899(v=VS.85).aspx">IAzOperation</a> object with the specified name from the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378186(v=VS.85).aspx">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified entity from the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378190(v=VS.85).aspx">DeleteTask</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/en-us/library/Aa378367(v=VS.85).aspx">IAzTask</a> object with the specified name from the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378210(v=VS.85).aspx">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzRole</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378228(v=VS.85).aspx">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>IAzRole</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378231(v=VS.85).aspx">Submit</a>
</td>
<td align="left" width="63%">
Persists changes made to the <b>IAzRole</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzRole</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378173(v=VS.85).aspx">ApplicationData</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves an opaque field that can be used by the application to store information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378176(v=VS.85).aspx">AppMembers</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the application groups that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378192(v=VS.85).aspx">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a comment that describes the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378213(v=VS.85).aspx">Members</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the text form of the SIDs of Windows  accounts that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378219(v=VS.85).aspx">MembersName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the account names of accounts that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378223(v=VS.85).aspx">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378225(v=VS.85).aspx">Operations</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the operations associated with the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378234(v=VS.85).aspx">Tasks</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the tasks associated with the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378235(v=VS.85).aspx">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the role can be modified by the  user context that initialized it.

</td>
</tr>
</table> 

