---
UID: NF:azroles.IAzApplicationGroup.GetProperty
title: IAzApplicationGroup::GetProperty
author: windows-sdk-content
description: Returns the IAzApplicationGroup object property with the specified property ID.
old-location: security\iazapplicationgroup_getproperty.htm
tech.root: SecAuthZ
ms.assetid: b91c21c0-3042-457b-9f53-b03d9805f255
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AZ_PROP_CHILD_CREATE, AZ_PROP_DESCRIPTION, AZ_PROP_GROUP_APP_MEMBERS, AZ_PROP_GROUP_APP_NON_MEMBERS, AZ_PROP_GROUP_LDAP_QUERY, AZ_PROP_GROUP_MEMBERS, AZ_PROP_GROUP_MEMBERS_NAME, AZ_PROP_GROUP_NON_MEMBERS, AZ_PROP_GROUP_NON_MEMBERS_NAME, AZ_PROP_GROUP_TYPE, AZ_PROP_NAME, AZ_PROP_WRITABLE, AzApplicationGroup object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzApplicationGroup object, GetProperty method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],GetProperty method, IAzApplicationGroup.GetProperty, IAzApplicationGroup::GetProperty, azroles/IAzApplicationGroup::GetProperty, security.iazapplicationgroup_getproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IAzApplicationGroup.GetProperty
 - AzApplicationGroup.GetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplicationGroup::GetProperty


## -description


The <b>GetProperty</b> method returns the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object property  with the specified property ID.


## -parameters




### -param lPropId [in]

Property ID of the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object property  to return. The following table shows the possible values.

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
Also accessed through the <a href="https://msdn.microsoft.com/b2ef8988-b4de-423f-b727-f69a789b98cf">Description</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_APP_MEMBERS"></a><a id="az_prop_group_app_members"></a><dl>
<dt><b>AZ_PROP_GROUP_APP_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/74239ac2-b6ea-4839-b4c5-7a77d454aa0b">AppMembers</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_APP_NON_MEMBERS"></a><a id="az_prop_group_app_non_members"></a><dl>
<dt><b>AZ_PROP_GROUP_APP_NON_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/a85a9004-f3f5-44ce-a0d7-fa450af74917">AppNonMembers</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_MEMBERS"></a><a id="az_prop_group_members"></a><dl>
<dt><b>AZ_PROP_GROUP_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/1370fe81-a729-477e-a500-1823abb713e1">Members</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_MEMBERS_NAME"></a><a id="az_prop_group_members_name"></a><dl>
<dt><b>AZ_PROP_GROUP_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/bdd6f88f-ea06-4075-b563-d0c7707107f8">MembersName</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_NON_MEMBERS"></a><a id="az_prop_group_non_members"></a><dl>
<dt><b>AZ_PROP_GROUP_NON_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/43bdd205-4750-4ff6-8063-8de2c5962b09">NonMembers</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_NON_MEMBERS_NAME"></a><a id="az_prop_group_non_members_name"></a><dl>
<dt><b>AZ_PROP_GROUP_NON_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/d78556ae-0d22-4df0-b850-dd7077fa3f85">NonMembersName</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_TYPE"></a><a id="az_prop_group_type"></a><dl>
<dt><b>AZ_PROP_GROUP_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/dc100895-4cfb-4e02-97bc-5c99bf26fbe2">Type</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_LDAP_QUERY"></a><a id="az_prop_group_ldap_query"></a><dl>
<dt><b>AZ_PROP_GROUP_LDAP_QUERY</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/963ee516-6dd5-419f-9186-578b7fe9c5bc">LdapQuery</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/a42fb625-d04e-4884-b644-2007f6dc52ba">Name</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_WRITABLE"></a><a id="az_prop_writable"></a><dl>
<dt><b>AZ_PROP_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/c0d88a7c-2df7-4f8e-94c2-75690d9758e7">Writable</a> property

</td>
</tr>
</table>
 


### -param varReserved [in, optional]

Reserved for future use.


### -param pvarProp [out]

A pointer to the returned <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object property.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.



