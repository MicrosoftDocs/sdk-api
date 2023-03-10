---
UID: NF:azroles.IAzApplicationGroup.GetProperty
title: IAzApplicationGroup::GetProperty (azroles.h)
description: Returns the IAzApplicationGroup object property with the specified property ID.
helpviewer_keywords: ["AZ_PROP_CHILD_CREATE","AZ_PROP_DESCRIPTION","AZ_PROP_GROUP_APP_MEMBERS","AZ_PROP_GROUP_APP_NON_MEMBERS","AZ_PROP_GROUP_LDAP_QUERY","AZ_PROP_GROUP_MEMBERS","AZ_PROP_GROUP_MEMBERS_NAME","AZ_PROP_GROUP_NON_MEMBERS","AZ_PROP_GROUP_NON_MEMBERS_NAME","AZ_PROP_GROUP_TYPE","AZ_PROP_NAME","AZ_PROP_WRITABLE","AzApplicationGroup object [Security]","GetProperty method","GetProperty","GetProperty method [Security]","GetProperty method [Security]","AzApplicationGroup object","GetProperty method [Security]","IAzApplicationGroup interface","IAzApplicationGroup interface [Security]","GetProperty method","IAzApplicationGroup.GetProperty","IAzApplicationGroup::GetProperty","azroles/IAzApplicationGroup::GetProperty","security.iazapplicationgroup_getproperty"]
old-location: security\iazapplicationgroup_getproperty.htm
tech.root: security
ms.assetid: b91c21c0-3042-457b-9f53-b03d9805f255
ms.date: 12/05/2018
ms.keywords: AZ_PROP_CHILD_CREATE, AZ_PROP_DESCRIPTION, AZ_PROP_GROUP_APP_MEMBERS, AZ_PROP_GROUP_APP_NON_MEMBERS, AZ_PROP_GROUP_LDAP_QUERY, AZ_PROP_GROUP_MEMBERS, AZ_PROP_GROUP_MEMBERS_NAME, AZ_PROP_GROUP_NON_MEMBERS, AZ_PROP_GROUP_NON_MEMBERS_NAME, AZ_PROP_GROUP_TYPE, AZ_PROP_NAME, AZ_PROP_WRITABLE, AzApplicationGroup object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzApplicationGroup object, GetProperty method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],GetProperty method, IAzApplicationGroup.GetProperty, IAzApplicationGroup::GetProperty, azroles/IAzApplicationGroup::GetProperty, security.iazapplicationgroup_getproperty
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
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzApplicationGroup::GetProperty
 - azroles/IAzApplicationGroup::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplicationGroup.GetProperty
 - AzApplicationGroup.GetProperty
---

# IAzApplicationGroup::GetProperty


## -description

The <b>GetProperty</b> method returns the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object property  with the specified property ID.

## -parameters

### -param lPropId [in]

Property ID of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object property  to return. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CHILD_CREATE"></a><a id="az_prop_child_create"></a><dl>
<dt><b>AZ_PROP_CHILD_CREATE</b></dt>
</dl>
</td>
<td width="60%">
Determines whether the current user has permission to create child objects. This value will always be <b>FALSE</b> because this object cannot have child objects.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_description">Description</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_APP_MEMBERS"></a><a id="az_prop_group_app_members"></a><dl>
<dt><b>AZ_PROP_GROUP_APP_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_appmembers">AppMembers</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_APP_NON_MEMBERS"></a><a id="az_prop_group_app_non_members"></a><dl>
<dt><b>AZ_PROP_GROUP_APP_NON_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_appnonmembers">AppNonMembers</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_MEMBERS"></a><a id="az_prop_group_members"></a><dl>
<dt><b>AZ_PROP_GROUP_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_members">Members</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_MEMBERS_NAME"></a><a id="az_prop_group_members_name"></a><dl>
<dt><b>AZ_PROP_GROUP_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_membersname">MembersName</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_NON_MEMBERS"></a><a id="az_prop_group_non_members"></a><dl>
<dt><b>AZ_PROP_GROUP_NON_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_nonmembers">NonMembers</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_NON_MEMBERS_NAME"></a><a id="az_prop_group_non_members_name"></a><dl>
<dt><b>AZ_PROP_GROUP_NON_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_nonmembersname">NonMembersName</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_TYPE"></a><a id="az_prop_group_type"></a><dl>
<dt><b>AZ_PROP_GROUP_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_type">Type</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_LDAP_QUERY"></a><a id="az_prop_group_ldap_query"></a><dl>
<dt><b>AZ_PROP_GROUP_LDAP_QUERY</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_ldapquery">LdapQuery</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_name">Name</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_WRITABLE"></a><a id="az_prop_writable"></a><dl>
<dt><b>AZ_PROP_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_writable">Writable</a> property

</td>
</tr>
</table>

### -param varReserved [in, optional]

Reserved for future use.

### -param pvarProp [out]

A pointer to the returned <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object property.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.