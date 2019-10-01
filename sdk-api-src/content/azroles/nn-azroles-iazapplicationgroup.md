---
UID: NN:azroles.IAzApplicationGroup
title: IAzApplicationGroup (azroles.h)
author: windows-sdk-content
description: Defines a collection of principals.
old-location: security\iazapplicationgroup.htm
tech.root: SecAuthZ
ms.assetid: 6a15acde-e582-4c49-b7e4-82d4e54012b1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAzApplicationGroup, IAzApplicationGroup interface [Security], IAzApplicationGroup interface [Security],described, azroles/IAzApplicationGroup, security.iazapplicationgroup
ms.topic: interface
f1_keywords: 
 - "azroles/IAzApplicationGroup"
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
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzApplicationGroup interface


## -description


The <b>IAzApplicationGroup</b> interface defines a collection of principals.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplicationGroup</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAzApplicationGroup</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-addappmember">AddAppMember</a>
</td>
<td align="left" width="63%">
Adds the specified <b>IAzApplicationGroup</b> object to the list of application groups that belong to this application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-addappnonmember">AddAppNonMember</a>
</td>
<td align="left" width="63%">
Adds the specified <b>IAzApplicationGroup</b> object to the list of application groups that are refused membership in this application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-addmember">AddMember</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) in text form to the list of  accounts that belong to the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-addmembername">AddMemberName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of  accounts that belong to the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-addnonmember">AddNonMember</a>
</td>
<td align="left" width="63%">
Adds the specified SID in text form to the list of  accounts that are refused membership in the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-addnonmembername">AddNonMemberName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of accounts that are refused membership in the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-addpropertyitem">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified entity to the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-deleteappmember">DeleteAppMember</a>
</td>
<td align="left" width="63%">
Removes the specified <b>IAzApplicationGroup</b> object from the list of application groups that belong to this application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-deleteappnonmember">DeleteAppNonMember</a>
</td>
<td align="left" width="63%">
Removes the specified <b>IAzApplicationGroup</b> object from the list of application groups that are refused membership in this application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-deletemember">DeleteMember</a>
</td>
<td align="left" width="63%">
Removes  the specified SID in text form from the list of  accounts that belong to the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-deletemembername">DeleteMemberName</a>
</td>
<td align="left" width="63%">
Removes  the specified account name from the list of   accounts that belong to the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-deletenonmember">DeleteNonMember</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of  accounts that are refused membership in the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-deletenonmembername">DeleteNonMemberName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of  accounts that are refused membership in the application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-deletepropertyitem">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified entity from the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzApplicationGroup</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>IAzApplicationGroup</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-submit">Submit</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_appmembers">AppMembers</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_appnonmembers">AppNonMembers</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_description">Description</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_ldapquery">LdapQuery</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/l-gly">Lightweight Directory Access Protocol</a> (LDAP) query used to define membership for an LDAP query application group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_members">Members</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_membersname">MembersName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_name">Name</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_nonmembers">NonMembers</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_nonmembersname">NonMembersName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_type">Type</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_writable">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the application group can be modified by the  user context that initialized it.

</td>
</tr>
</table> 

