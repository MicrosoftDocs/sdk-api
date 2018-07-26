---
UID: NF:azroles.IAzApplicationGroup.DeletePropertyItem
title: IAzApplicationGroup::DeletePropertyItem
author: windows-sdk-content
description: Removes the specified entity from the specified list.
old-location: security\iazapplicationgroup_deletepropertyitem.htm
old-project: secauthz
ms.assetid: 63ed036a-ad1d-47a8-a4c7-f23fc060c2db
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: AZ_PROP_GROUP_APP_MEMBERS, AZ_PROP_GROUP_APP_NON_MEMBERS, AZ_PROP_GROUP_MEMBERS, AZ_PROP_GROUP_MEMBERS_NAME, AZ_PROP_GROUP_NON_MEMBERS, AZ_PROP_GROUP_NON_MEMBERS_NAME, AzApplicationGroup object [Security],DeletePropertyItem method, DeletePropertyItem, DeletePropertyItem method [Security], DeletePropertyItem method [Security],AzApplicationGroup object, DeletePropertyItem method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],DeletePropertyItem method, IAzApplicationGroup.DeletePropertyItem, IAzApplicationGroup::DeletePropertyItem, azroles/IAzApplicationGroup::DeletePropertyItem, security.iazapplicationgroup_deletepropertyitem
ms.prod: windows
ms.technology: windows-sdk
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
 - IAzApplicationGroup.DeletePropertyItem
 - AzApplicationGroup.DeletePropertyItem
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
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
Can also be removed using the <a href="https://msdn.microsoft.com/856d9b18-927a-462a-b238-78b704bcc58b">DeleteAppMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_APP_NON_MEMBERS"></a><a id="az_prop_group_app_non_members"></a><dl>
<dt><b>AZ_PROP_GROUP_APP_NON_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/d78f3cd9-4ccb-47b7-98bd-5e69ebbb178c">DeleteAppNonMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_MEMBERS"></a><a id="az_prop_group_members"></a><dl>
<dt><b>AZ_PROP_GROUP_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/9db3b162-b37d-4a86-a3c0-cb594370238b">DeleteMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_MEMBERS_NAME"></a><a id="az_prop_group_members_name"></a><dl>
<dt><b>AZ_PROP_GROUP_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/3b3a8aee-b1ef-464a-9b67-80b703d41d69">DeleteMemberName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_NON_MEMBERS"></a><a id="az_prop_group_non_members"></a><dl>
<dt><b>AZ_PROP_GROUP_NON_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/05d58f62-fa34-4829-a535-65ea0f5144ab">DeleteNonMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_NON_MEMBERS_NAME"></a><a id="az_prop_group_non_members_name"></a><dl>
<dt><b>AZ_PROP_GROUP_NON_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/8011e55a-1e62-45a6-a91c-07a488384d84">DeleteNonMemberName</a> method

</td>
</tr>
</table>
 


### -param varProp [in]

The entity to remove from the list  specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

If AZ_PROP_GROUP_MEMBERS_NAME or AZ_PROP_GROUP_NON_MEMBERS_NAME is specified for the <i>lPropId</i> parameter, the string is the account name of the account to remove from the list. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). If AZ_PROP_GROUP_APP_MEMBERS or AZ_PROP_GROUP_APP_NON_MEMBERS is specified for the <i>lPropId</i> parameter, the string is the  <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> property of the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to remove from the list.


### -param varReserved [in, optional]

Reserved for future use.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.



