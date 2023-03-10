---
UID: NF:azroles.IAzApplicationGroup.AddPropertyItem
title: IAzApplicationGroup::AddPropertyItem (azroles.h)
description: Adds the specified entity to the specified list. (IAzApplicationGroup.AddPropertyItem)
helpviewer_keywords: ["AZ_PROP_GROUP_APP_MEMBERS","AZ_PROP_GROUP_APP_NON_MEMBERS","AZ_PROP_GROUP_MEMBERS","AZ_PROP_GROUP_MEMBERS_NAME","AZ_PROP_GROUP_NON_MEMBERS","AZ_PROP_GROUP_NON_MEMBERS_NAME","AddPropertyItem","AddPropertyItem method [Security]","AddPropertyItem method [Security]","AzApplicationGroup object","AddPropertyItem method [Security]","IAzApplicationGroup interface","AzApplicationGroup object [Security]","AddPropertyItem method","IAzApplicationGroup interface [Security]","AddPropertyItem method","IAzApplicationGroup.AddPropertyItem","IAzApplicationGroup::AddPropertyItem","azroles/IAzApplicationGroup::AddPropertyItem","security.iazapplicationgroup_addpropertyitem"]
old-location: security\iazapplicationgroup_addpropertyitem.htm
tech.root: security
ms.assetid: 7a7a11ad-42f9-4d3f-8d55-6e8b3e1bea7e
ms.date: 12/05/2018
ms.keywords: AZ_PROP_GROUP_APP_MEMBERS, AZ_PROP_GROUP_APP_NON_MEMBERS, AZ_PROP_GROUP_MEMBERS, AZ_PROP_GROUP_MEMBERS_NAME, AZ_PROP_GROUP_NON_MEMBERS, AZ_PROP_GROUP_NON_MEMBERS_NAME, AddPropertyItem, AddPropertyItem method [Security], AddPropertyItem method [Security],AzApplicationGroup object, AddPropertyItem method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddPropertyItem method, IAzApplicationGroup interface [Security],AddPropertyItem method, IAzApplicationGroup.AddPropertyItem, IAzApplicationGroup::AddPropertyItem, azroles/IAzApplicationGroup::AddPropertyItem, security.iazapplicationgroup_addpropertyitem
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
 - IAzApplicationGroup::AddPropertyItem
 - azroles/IAzApplicationGroup::AddPropertyItem
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
 - IAzApplicationGroup.AddPropertyItem
 - AzApplicationGroup.AddPropertyItem
---

# IAzApplicationGroup::AddPropertyItem


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
<td width="40%"><a id="AZ_PROP_GROUP_APP_MEMBERS"></a><a id="az_prop_group_app_members"></a><dl>
<dt><b>AZ_PROP_GROUP_APP_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-addappmember">AddAppMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_APP_NON_MEMBERS"></a><a id="az_prop_group_app_non_members"></a><dl>
<dt><b>AZ_PROP_GROUP_APP_NON_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-addappnonmember">AddAppNonMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_MEMBERS"></a><a id="az_prop_group_members"></a><dl>
<dt><b>AZ_PROP_GROUP_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-addmember">AddMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_MEMBERS_NAME"></a><a id="az_prop_group_members_name"></a><dl>
<dt><b>AZ_PROP_GROUP_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-addmembername">AddMemberName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_NON_MEMBERS"></a><a id="az_prop_group_non_members"></a><dl>
<dt><b>AZ_PROP_GROUP_NON_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-addnonmember">AddNonMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_NON_MEMBERS_NAME"></a><a id="az_prop_group_non_members_name"></a><dl>
<dt><b>AZ_PROP_GROUP_NON_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-addnonmembername">AddNonMemberName</a> method

</td>
</tr>
</table>

### -param varProp

TBD

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-submit">Submit</a> method to persist any changes made by this method.
