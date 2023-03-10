---
UID: NF:azroles.IAzApplicationGroup.DeletePropertyItem
title: IAzApplicationGroup::DeletePropertyItem (azroles.h)
description: Removes the specified entity from the specified list. (IAzApplicationGroup.DeletePropertyItem)
helpviewer_keywords: ["AZ_PROP_GROUP_APP_MEMBERS","AZ_PROP_GROUP_APP_NON_MEMBERS","AZ_PROP_GROUP_MEMBERS","AZ_PROP_GROUP_MEMBERS_NAME","AZ_PROP_GROUP_NON_MEMBERS","AZ_PROP_GROUP_NON_MEMBERS_NAME","AzApplicationGroup object [Security]","DeletePropertyItem method","DeletePropertyItem","DeletePropertyItem method [Security]","DeletePropertyItem method [Security]","AzApplicationGroup object","DeletePropertyItem method [Security]","IAzApplicationGroup interface","IAzApplicationGroup interface [Security]","DeletePropertyItem method","IAzApplicationGroup.DeletePropertyItem","IAzApplicationGroup::DeletePropertyItem","azroles/IAzApplicationGroup::DeletePropertyItem","security.iazapplicationgroup_deletepropertyitem"]
old-location: security\iazapplicationgroup_deletepropertyitem.htm
tech.root: security
ms.assetid: 63ed036a-ad1d-47a8-a4c7-f23fc060c2db
ms.date: 12/05/2018
ms.keywords: AZ_PROP_GROUP_APP_MEMBERS, AZ_PROP_GROUP_APP_NON_MEMBERS, AZ_PROP_GROUP_MEMBERS, AZ_PROP_GROUP_MEMBERS_NAME, AZ_PROP_GROUP_NON_MEMBERS, AZ_PROP_GROUP_NON_MEMBERS_NAME, AzApplicationGroup object [Security],DeletePropertyItem method, DeletePropertyItem, DeletePropertyItem method [Security], DeletePropertyItem method [Security],AzApplicationGroup object, DeletePropertyItem method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],DeletePropertyItem method, IAzApplicationGroup.DeletePropertyItem, IAzApplicationGroup::DeletePropertyItem, azroles/IAzApplicationGroup::DeletePropertyItem, security.iazapplicationgroup_deletepropertyitem
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
 - IAzApplicationGroup::DeletePropertyItem
 - azroles/IAzApplicationGroup::DeletePropertyItem
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
 - IAzApplicationGroup.DeletePropertyItem
 - AzApplicationGroup.DeletePropertyItem
---

# IAzApplicationGroup::DeletePropertyItem


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
<td width="40%"><a id="AZ_PROP_GROUP_APP_MEMBERS"></a><a id="az_prop_group_app_members"></a><dl>
<dt><b>AZ_PROP_GROUP_APP_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-deleteappmember">DeleteAppMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_APP_NON_MEMBERS"></a><a id="az_prop_group_app_non_members"></a><dl>
<dt><b>AZ_PROP_GROUP_APP_NON_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-deleteappnonmember">DeleteAppNonMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_MEMBERS"></a><a id="az_prop_group_members"></a><dl>
<dt><b>AZ_PROP_GROUP_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-deletemember">DeleteMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_MEMBERS_NAME"></a><a id="az_prop_group_members_name"></a><dl>
<dt><b>AZ_PROP_GROUP_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-deletemembername">DeleteMemberName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_NON_MEMBERS"></a><a id="az_prop_group_non_members"></a><dl>
<dt><b>AZ_PROP_GROUP_NON_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-deletenonmember">DeleteNonMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_NON_MEMBERS_NAME"></a><a id="az_prop_group_non_members_name"></a><dl>
<dt><b>AZ_PROP_GROUP_NON_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-deletenonmembername">DeleteNonMemberName</a> method

</td>
</tr>
</table>

### -param varProp [in]

The entity to remove from the list  specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

If AZ_PROP_GROUP_MEMBERS_NAME or AZ_PROP_GROUP_NON_MEMBERS_NAME is specified for the <i>lPropId</i> parameter, the string is the account name of the account to remove from the list. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). If AZ_PROP_GROUP_APP_MEMBERS or AZ_PROP_GROUP_APP_NON_MEMBERS is specified for the <i>lPropId</i> parameter, the string is the  <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_name">Name</a> property of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object to remove from the list.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.
