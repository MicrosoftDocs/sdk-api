---
UID: NF:azroles.IAzRole.DeletePropertyItem
title: IAzRole::DeletePropertyItem (azroles.h)
description: Removes the specified entity from the specified list. (IAzRole.DeletePropertyItem)
helpviewer_keywords: ["AZ_PROP_ROLE_APP_MEMBERS","AZ_PROP_ROLE_MEMBERS","AZ_PROP_ROLE_MEMBERS_NAME","AZ_PROP_ROLE_OPERATIONS","AZ_PROP_ROLE_TASKS","AzRole object [Security]","DeletePropertyItem method","DeletePropertyItem","DeletePropertyItem method [Security]","DeletePropertyItem method [Security]","AzRole object","DeletePropertyItem method [Security]","IAzRole interface","IAzRole interface [Security]","DeletePropertyItem method","IAzRole.DeletePropertyItem","IAzRole::DeletePropertyItem","azroles/IAzRole::DeletePropertyItem","security.iazrole_deletepropertyitem"]
old-location: security\iazrole_deletepropertyitem.htm
tech.root: security
ms.assetid: 79315dbc-70b4-4667-8187-9b26b971baee
ms.date: 12/05/2018
ms.keywords: AZ_PROP_ROLE_APP_MEMBERS, AZ_PROP_ROLE_MEMBERS, AZ_PROP_ROLE_MEMBERS_NAME, AZ_PROP_ROLE_OPERATIONS, AZ_PROP_ROLE_TASKS, AzRole object [Security],DeletePropertyItem method, DeletePropertyItem, DeletePropertyItem method [Security], DeletePropertyItem method [Security],AzRole object, DeletePropertyItem method [Security],IAzRole interface, IAzRole interface [Security],DeletePropertyItem method, IAzRole.DeletePropertyItem, IAzRole::DeletePropertyItem, azroles/IAzRole::DeletePropertyItem, security.iazrole_deletepropertyitem
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
 - IAzRole::DeletePropertyItem
 - azroles/IAzRole::DeletePropertyItem
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
 - IAzRole.DeletePropertyItem
 - AzRole.DeletePropertyItem
---

# IAzRole::DeletePropertyItem


## -description

The <b>DeletePropertyItem</b> method removes the specified entity from the specified list.

## -parameters

### -param lPropId [in]

Property ID of the  list from which to remove the entity specified by the <i>varProp</i> parameter. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_APP_MEMBERS"></a><a id="az_prop_role_app_members"></a><dl>
<dt><b>AZ_PROP_ROLE_APP_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-deleteappmember">DeleteAppMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_MEMBERS"></a><a id="az_prop_role_members"></a><dl>
<dt><b>AZ_PROP_ROLE_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-deletemember">DeleteMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_MEMBERS_NAME"></a><a id="az_prop_role_members_name"></a><dl>
<dt><b>AZ_PROP_ROLE_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-deletemembername">DeleteMemberName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_OPERATIONS"></a><a id="az_prop_role_operations"></a><dl>
<dt><b>AZ_PROP_ROLE_OPERATIONS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-deleteoperation">DeleteOperation</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_TASKS"></a><a id="az_prop_role_tasks"></a><dl>
<dt><b>AZ_PROP_ROLE_TASKS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-deletetask">DeleteTask</a> method

</td>
</tr>
</table>

### -param varProp [in]

Entity to remove from the list  specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

If AZ_PROP_ROLE_MEMBERS is specified for the <i>lPropId</i> parameter, the string is the  <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) of the Windows account to remove from the list. If AZ_PROP_ROLE_MEMBERS_NAME is specified for the <i>lPropId</i> parameter, the string is the account name of the account to remove from the list. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the "ExampleDomain\UserName" format. If AZ_PROP_ROLE_APP_MEMBERS is specified for the <i>lPropId</i> parameter, the string is the  <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_name">Name</a> property of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object to remove from the list.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.
