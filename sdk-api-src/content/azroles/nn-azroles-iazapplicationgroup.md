---
UID: NN:azroles.IAzApplicationGroup
title: IAzApplicationGroup
author: windows-sdk-content
description: Defines a collection of principals.
old-location: security\iazapplicationgroup.htm
old-project: SecAuthZ
ms.assetid: 6a15acde-e582-4c49-b7e4-82d4e54012b1
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IAzApplicationGroup, IAzApplicationGroup interface [Security], IAzApplicationGroup interface [Security],described, azroles/IAzApplicationGroup, security.iazapplicationgroup
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
 - IAzApplicationGroup
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplicationGroup interface


## -description


The <b>IAzApplicationGroup</b> interface defines a collection of principals.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplicationGroup</b> interface inherits from the <a href="http://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IAzApplicationGroup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzApplicationGroup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35b6c928-0c11-420d-8ba7-f28b0c67f55d">AddAppMember</a>
</td>
<td align="left" width="63%">
Adds the specified <b>IAzApplicationGroup</b> object to the list of application groups that belong to this application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31b8538f-afe1-4fd3-bf6f-6f3f0641fc2a">AddAppNonMember</a>
</td>
<td align="left" width="63%">
Adds the specified <b>IAzApplicationGroup</b> object to the list of application groups that are refused membership in this application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/934ca397-2067-451a-bccd-103ab4db3b1f">AddMember</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form to the list of  accounts that belong to the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/148be96b-be8d-4ad7-a5ad-f22599114cfa">AddMemberName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of  accounts that belong to the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a61f0b97-cd8a-40e5-b2ef-8eb48359fead">AddNonMember</a>
</td>
<td align="left" width="63%">
Adds the specified SID in text form to the list of  accounts that are refused membership in the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56bde3d9-f4f7-449d-a080-5215dda940a0">AddNonMemberName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of accounts that are refused membership in the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a7a11ad-42f9-4d3f-8d55-6e8b3e1bea7e">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified entity to the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/856d9b18-927a-462a-b238-78b704bcc58b">DeleteAppMember</a>
</td>
<td align="left" width="63%">
Removes the specified <b>IAzApplicationGroup</b> object from the list of application groups that belong to this application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d78f3cd9-4ccb-47b7-98bd-5e69ebbb178c">DeleteAppNonMember</a>
</td>
<td align="left" width="63%">
Removes the specified <b>IAzApplicationGroup</b> object from the list of application groups that are refused membership in this application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9db3b162-b37d-4a86-a3c0-cb594370238b">DeleteMember</a>
</td>
<td align="left" width="63%">
Removes  the specified SID in text form from the list of  accounts that belong to the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b3a8aee-b1ef-464a-9b67-80b703d41d69">DeleteMemberName</a>
</td>
<td align="left" width="63%">
Removes  the specified account name from the list of   accounts that belong to the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05d58f62-fa34-4829-a535-65ea0f5144ab">DeleteNonMember</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of  accounts that are refused membership in the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8011e55a-1e62-45a6-a91c-07a488384d84">DeleteNonMemberName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of  accounts that are refused membership in the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63ed036a-ad1d-47a8-a4c7-f23fc060c2db">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified entity from the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b91c21c0-3042-457b-9f53-b03d9805f255">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzApplicationGroup</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1af01f2-bd86-4404-a281-2024777dafaa">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>IAzApplicationGroup</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51a855dd-4a90-4f7a-b32f-f91e3941655b">Submit</a>
</td>
<td align="left" width="63%">
Persists changes made to the <b>IAzApplicationGroup</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplicationGroup</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/74239ac2-b6ea-4839-b4c5-7a77d454aa0b">AppMembers</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the application groups that belong to this application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a85a9004-f3f5-44ce-a0d7-fa450af74917">AppNonMembers</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the application groups that are refused membership in this application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a comment that describes the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/963ee516-6dd5-419f-9186-578b7fe9c5bc">LdapQuery</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Lightweight Directory Access Protocol</a> (LDAP) query used to define membership for an LDAP query application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1370fe81-a729-477e-a500-1823abb713e1">Members</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the SIDs (in text form) of  accounts that belong to the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bdd6f88f-ea06-4075-b563-d0c7707107f8">MembersName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the account names of accounts that belong to the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/43bdd205-4750-4ff6-8063-8de2c5962b09">NonMembers</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the SIDs (in text form) of  accounts that are refused membership in  the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d78556ae-0d22-4df0-b850-dd7077fa3f85">NonMembersName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the account names of accounts that are refused membership in  the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the group type of the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c0d88a7c-2df7-4f8e-94c2-75690d9758e7">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the application group can be modified by the  user context that initialized it.

</td>
</tr>
</table> 

