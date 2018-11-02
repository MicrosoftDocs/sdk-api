---
UID: NN:azroles.IAzApplicationGroup
title: IAzApplicationGroup
author: windows-sdk-content
description: Defines a collection of principals.
old-location: security\iazapplicationgroup.htm
tech.root: secauthz
ms.assetid: 6a15acde-e582-4c49-b7e4-82d4e54012b1
ms.author: windowssdkdev
ms.date: 10/30/2018
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
 - IAzApplicationGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplicationGroup interface


## -description


The <b>IAzApplicationGroup</b> interface defines a collection of principals.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplicationGroup</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAzApplicationGroup</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377303(v=VS.85).aspx">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified entity to the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377306(v=VS.85).aspx">DeleteAppMember</a>
</td>
<td align="left" width="63%">
Removes the specified <b>IAzApplicationGroup</b> object from the list of application groups that belong to this application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377307(v=VS.85).aspx">DeleteAppNonMember</a>
</td>
<td align="left" width="63%">
Removes the specified <b>IAzApplicationGroup</b> object from the list of application groups that are refused membership in this application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377308(v=VS.85).aspx">DeleteMember</a>
</td>
<td align="left" width="63%">
Removes  the specified SID in text form from the list of  accounts that belong to the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377309(v=VS.85).aspx">DeleteMemberName</a>
</td>
<td align="left" width="63%">
Removes  the specified account name from the list of   accounts that belong to the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377310(v=VS.85).aspx">DeleteNonMember</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of  accounts that are refused membership in the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377311(v=VS.85).aspx">DeleteNonMemberName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of  accounts that are refused membership in the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377312(v=VS.85).aspx">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified entity from the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377314(v=VS.85).aspx">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzApplicationGroup</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377321(v=VS.85).aspx">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>IAzApplicationGroup</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377322(v=VS.85).aspx">Submit</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa377304(v=VS.85).aspx">AppMembers</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377305(v=VS.85).aspx">AppNonMembers</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377313(v=VS.85).aspx">Description</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377315(v=VS.85).aspx">LdapQuery</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms721592(v=VS.85).aspx">Lightweight Directory Access Protocol</a> (LDAP) query used to define membership for an LDAP query application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377316(v=VS.85).aspx">Members</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377317(v=VS.85).aspx">MembersName</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377318(v=VS.85).aspx">Name</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377319(v=VS.85).aspx">NonMembers</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377320(v=VS.85).aspx">NonMembersName</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377323(v=VS.85).aspx">Type</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377324(v=VS.85).aspx">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the application group can be modified by the  user context that initialized it.

</td>
</tr>
</table> 

