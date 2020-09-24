---
UID: NF:azroles.IAzRole.GetProperty
title: IAzRole::GetProperty (azroles.h)
description: Returns the IAzRole object property with the specified property ID.
helpviewer_keywords: ["AZ_PROP_APPLICATION_DATA","AZ_PROP_CHILD_CREATE","AZ_PROP_DESCRIPTION","AZ_PROP_NAME","AZ_PROP_ROLE_APP_MEMBERS","AZ_PROP_ROLE_MEMBERS","AZ_PROP_ROLE_MEMBERS_NAME","AZ_PROP_ROLE_OPERATIONS","AZ_PROP_ROLE_TASKS","AZ_PROP_WRITABLE","AzRole object [Security]","GetProperty method","GetProperty","GetProperty method [Security]","GetProperty method [Security]","AzRole object","GetProperty method [Security]","IAzRole interface","IAzRole interface [Security]","GetProperty method","IAzRole.GetProperty","IAzRole::GetProperty","azroles/IAzRole::GetProperty","security.iazrole_getproperty"]
old-location: security\iazrole_getproperty.htm
tech.root: security
ms.assetid: f65058ce-962d-4cad-9f55-c8b983ffaa05
ms.date: 12/05/2018
ms.keywords: AZ_PROP_APPLICATION_DATA, AZ_PROP_CHILD_CREATE, AZ_PROP_DESCRIPTION, AZ_PROP_NAME, AZ_PROP_ROLE_APP_MEMBERS, AZ_PROP_ROLE_MEMBERS, AZ_PROP_ROLE_MEMBERS_NAME, AZ_PROP_ROLE_OPERATIONS, AZ_PROP_ROLE_TASKS, AZ_PROP_WRITABLE, AzRole object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzRole object, GetProperty method [Security],IAzRole interface, IAzRole interface [Security],GetProperty method, IAzRole.GetProperty, IAzRole::GetProperty, azroles/IAzRole::GetProperty, security.iazrole_getproperty
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
 - IAzRole::GetProperty
 - azroles/IAzRole::GetProperty
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
 - IAzRole.GetProperty
 - AzRole.GetProperty
---

# IAzRole::GetProperty


## -description

The <b>GetProperty</b> method returns the <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object property  with the specified property ID.

## -parameters

### -param lPropId [in]

Property ID of the <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object property  to return. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_DATA"></a><a id="az_prop_application_data"></a><dl>
<dt><b>AZ_PROP_APPLICATION_DATA</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_applicationdata">ApplicationData</a>  property

</td>
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
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_description">Description</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_name">Name</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_APP_MEMBERS"></a><a id="az_prop_role_app_members"></a><dl>
<dt><b>AZ_PROP_ROLE_APP_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_appmembers">AppMembers</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_MEMBERS"></a><a id="az_prop_role_members"></a><dl>
<dt><b>AZ_PROP_ROLE_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_members">Members</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_MEMBERS_NAME"></a><a id="az_prop_role_members_name"></a><dl>
<dt><b>AZ_PROP_ROLE_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_membersname">MembersName</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_OPERATIONS"></a><a id="az_prop_role_operations"></a><dl>
<dt><b>AZ_PROP_ROLE_OPERATIONS</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_operations">Operations</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_TASKS"></a><a id="az_prop_role_tasks"></a><dl>
<dt><b>AZ_PROP_ROLE_TASKS</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_tasks">Tasks</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_WRITABLE"></a><a id="az_prop_writable"></a><dl>
<dt><b>AZ_PROP_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_writable">Writable</a>  property

</td>
</tr>
</table>

### -param varReserved [in, optional]

Reserved for future use.

### -param pvarProp [out]

A pointer to the returned <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object property.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.