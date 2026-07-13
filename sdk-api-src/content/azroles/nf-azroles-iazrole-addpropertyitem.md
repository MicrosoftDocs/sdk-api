---
UID: NF:azroles.IAzRole.AddPropertyItem
title: IAzRole::AddPropertyItem (azroles.h)
description: Adds the specified entity to the specified list. (IAzRole.AddPropertyItem)
helpviewer_keywords: ["AZ_PROP_ROLE_APP_MEMBERS","AZ_PROP_ROLE_MEMBERS","AZ_PROP_ROLE_MEMBERS_NAME","AZ_PROP_ROLE_OPERATIONS","AZ_PROP_ROLE_TASKS","AddPropertyItem","AddPropertyItem method [Security]","AddPropertyItem method [Security]","AzRole object","AddPropertyItem method [Security]","IAzRole interface","AzRole object [Security]","AddPropertyItem method","IAzRole interface [Security]","AddPropertyItem method","IAzRole.AddPropertyItem","IAzRole::AddPropertyItem","azroles/IAzRole::AddPropertyItem","security.iazrole_addpropertyitem"]
old-location: security\iazrole_addpropertyitem.htm
tech.root: security
ms.assetid: 3d9cb227-a3e8-4cd3-806a-5b7a38661b71
ms.date: 12/05/2018
ms.keywords: AZ_PROP_ROLE_APP_MEMBERS, AZ_PROP_ROLE_MEMBERS, AZ_PROP_ROLE_MEMBERS_NAME, AZ_PROP_ROLE_OPERATIONS, AZ_PROP_ROLE_TASKS, AddPropertyItem, AddPropertyItem method [Security], AddPropertyItem method [Security],AzRole object, AddPropertyItem method [Security],IAzRole interface, AzRole object [Security],AddPropertyItem method, IAzRole interface [Security],AddPropertyItem method, IAzRole.AddPropertyItem, IAzRole::AddPropertyItem, azroles/IAzRole::AddPropertyItem, security.iazrole_addpropertyitem
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
 - IAzRole::AddPropertyItem
 - azroles/IAzRole::AddPropertyItem
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
 - IAzRole.AddPropertyItem
 - AzRole.AddPropertyItem
---

# IAzRole::AddPropertyItem


## -description

The <b>AddPropertyItem</b> method adds the specified entity to the specified list.

## -parameters

### -param lPropId [in]

Property ID of the  list to which to add the entity specified by the <i>varProp</i> parameter. The following table shows the possible values.

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
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-addappmember">AddAppMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_MEMBERS"></a><a id="az_prop_role_members"></a><dl>
<dt><b>AZ_PROP_ROLE_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-addmember">AddMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_MEMBERS_NAME"></a><a id="az_prop_role_members_name"></a><dl>
<dt><b>AZ_PROP_ROLE_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-addmembername">AddMemberName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_OPERATIONS"></a><a id="az_prop_role_operations"></a><dl>
<dt><b>AZ_PROP_ROLE_OPERATIONS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-addoperation">AddOperation</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_TASKS"></a><a id="az_prop_role_tasks"></a><dl>
<dt><b>AZ_PROP_ROLE_TASKS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-addtask">AddTask</a> method

</td>
</tr>
</table>

### -param varProp [in]

Entity to add to the list  specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

If AZ_PROP_ROLE_MEMBERS is specified for the <i>lPropId</i> parameter, the string is the text form of the   <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) of the Windows account to add to the list. If AZ_PROP_ROLE_MEMBERS_NAME is specified for the <i>lPropId</i> parameter, the string is the account name of the account to add to the list. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the  "ExampleDomain\UserName" format. If AZ_PROP_ROLE_APP_MEMBERS is specified for the <i>lPropId</i> parameter, the string is the  <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_name">Name</a> property of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object to add to the list.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-submit">Submit</a> method to persist any changes made by this method.
