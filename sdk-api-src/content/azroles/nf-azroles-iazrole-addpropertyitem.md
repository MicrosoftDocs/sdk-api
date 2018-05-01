---
UID: NF:azroles.IAzRole.AddPropertyItem
title: IAzRole::AddPropertyItem method
author: windows-driver-content
description: Adds the specified entity to the specified list.
old-location: security\iazrole_addpropertyitem.htm
old-project: SecAuthZ
ms.assetid: 3d9cb227-a3e8-4cd3-806a-5b7a38661b71
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AZ_PROP_ROLE_APP_MEMBERS, AZ_PROP_ROLE_MEMBERS, AZ_PROP_ROLE_MEMBERS_NAME, AZ_PROP_ROLE_OPERATIONS, AZ_PROP_ROLE_TASKS, AddPropertyItem method [Security], AddPropertyItem method [Security], AzRole object, AddPropertyItem method [Security], IAzRole interface, AddPropertyItem,IAzRole.AddPropertyItem, AzRole object [Security], AddPropertyItem method, IAzRole, IAzRole interface [Security], AddPropertyItem method, IAzRole::AddPropertyItem, azroles/IAzRole::AddPropertyItem, security.iazrole_addpropertyitem
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzRole.AddPropertyItem
-	AzRole.AddPropertyItem
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzRole::AddPropertyItem method


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
Can also be added using the <a href="https://msdn.microsoft.com/118387f8-a422-4a8d-9d12-a5b5ee1e7b06">AddAppMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_MEMBERS"></a><a id="az_prop_role_members"></a><dl>
<dt><b>AZ_PROP_ROLE_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="https://msdn.microsoft.com/b2be62cb-7256-4031-8af9-24f3043a8430">AddMember</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_MEMBERS_NAME"></a><a id="az_prop_role_members_name"></a><dl>
<dt><b>AZ_PROP_ROLE_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="https://msdn.microsoft.com/fc2ca62e-40b1-4b09-a129-50d6162c6807">AddMemberName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_OPERATIONS"></a><a id="az_prop_role_operations"></a><dl>
<dt><b>AZ_PROP_ROLE_OPERATIONS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="https://msdn.microsoft.com/8c6d26ff-3287-4a1d-91cb-759f79ec92e5">AddOperation</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_TASKS"></a><a id="az_prop_role_tasks"></a><dl>
<dt><b>AZ_PROP_ROLE_TASKS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="https://msdn.microsoft.com/51ba30c3-8067-4aca-b8aa-8e64d4427b98">AddTask</a> method

</td>
</tr>
</table>
 


### -param varProp [in]

Entity to add to the list  specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

If AZ_PROP_ROLE_MEMBERS is specified for the <i>lPropId</i> parameter, the string is the text form of the   <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) of the Windows account to add to the list. If AZ_PROP_ROLE_MEMBERS_NAME is specified for the <i>lPropId</i> parameter, the string is the account name of the account to add to the list. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the  "ExampleDomain\UserName" format. If AZ_PROP_ROLE_APP_MEMBERS is specified for the <i>lPropId</i> parameter, the string is the  <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> property of the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to add to the list.


### -param varReserved [in, optional]

Reserved for future use.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/97f2018a-92f0-4ebb-85f1-78c140003d8f">Submit</a> method to persist any changes made by this method.



