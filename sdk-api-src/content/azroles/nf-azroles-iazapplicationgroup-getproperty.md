---
UID: NF:azroles.IAzApplicationGroup.GetProperty
title: IAzApplicationGroup::GetProperty
author: windows-sdk-content
description: Returns the IAzApplicationGroup object property with the specified property ID.
old-location: security\iazapplicationgroup_getproperty.htm
old-project: secauthz
ms.assetid: b91c21c0-3042-457b-9f53-b03d9805f255
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AZ_PROP_CHILD_CREATE, AZ_PROP_DESCRIPTION, AZ_PROP_GROUP_APP_MEMBERS, AZ_PROP_GROUP_APP_NON_MEMBERS, AZ_PROP_GROUP_LDAP_QUERY, AZ_PROP_GROUP_MEMBERS, AZ_PROP_GROUP_MEMBERS_NAME, AZ_PROP_GROUP_NON_MEMBERS, AZ_PROP_GROUP_NON_MEMBERS_NAME, AZ_PROP_GROUP_TYPE, AZ_PROP_NAME, AZ_PROP_WRITABLE, AzApplicationGroup object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzApplicationGroup object, GetProperty method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],GetProperty method, IAzApplicationGroup.GetProperty, IAzApplicationGroup::GetProperty, azroles/IAzApplicationGroup::GetProperty, security.iazapplicationgroup_getproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
 - IAzApplicationGroup.GetProperty
 - AzApplicationGroup.GetProperty
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplicationGroup::GetProperty


## -description


The <b>GetProperty</b> method returns the <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object property  with the specified property ID.


## -parameters




### -param lPropId [in]

Property ID of the <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object property  to return. The following table shows the possible values.

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
Also accessed through the <a href="https://msdn.microsoft.com/en-us/library/Aa377313(v=VS.85).aspx">Description</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_APP_MEMBERS"></a><a id="az_prop_group_app_members"></a><dl>
<dt><b>AZ_PROP_GROUP_APP_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/en-us/library/Aa377304(v=VS.85).aspx">AppMembers</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_APP_NON_MEMBERS"></a><a id="az_prop_group_app_non_members"></a><dl>
<dt><b>AZ_PROP_GROUP_APP_NON_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/en-us/library/Aa377305(v=VS.85).aspx">AppNonMembers</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_MEMBERS"></a><a id="az_prop_group_members"></a><dl>
<dt><b>AZ_PROP_GROUP_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/en-us/library/Aa377316(v=VS.85).aspx">Members</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_MEMBERS_NAME"></a><a id="az_prop_group_members_name"></a><dl>
<dt><b>AZ_PROP_GROUP_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/en-us/library/Aa377317(v=VS.85).aspx">MembersName</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_NON_MEMBERS"></a><a id="az_prop_group_non_members"></a><dl>
<dt><b>AZ_PROP_GROUP_NON_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/en-us/library/Aa377319(v=VS.85).aspx">NonMembers</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_NON_MEMBERS_NAME"></a><a id="az_prop_group_non_members_name"></a><dl>
<dt><b>AZ_PROP_GROUP_NON_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/en-us/library/Aa377320(v=VS.85).aspx">NonMembersName</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_TYPE"></a><a id="az_prop_group_type"></a><dl>
<dt><b>AZ_PROP_GROUP_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/en-us/library/Aa377323(v=VS.85).aspx">Type</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_LDAP_QUERY"></a><a id="az_prop_group_ldap_query"></a><dl>
<dt><b>AZ_PROP_GROUP_LDAP_QUERY</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/en-us/library/Aa377315(v=VS.85).aspx">LdapQuery</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/en-us/library/Aa377318(v=VS.85).aspx">Name</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_WRITABLE"></a><a id="az_prop_writable"></a><dl>
<dt><b>AZ_PROP_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/en-us/library/Aa377324(v=VS.85).aspx">Writable</a> property

</td>
</tr>
</table>
 


### -param varReserved [in, optional]

Reserved for future use.


### -param pvarProp [out]

A pointer to the returned <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object property.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.



