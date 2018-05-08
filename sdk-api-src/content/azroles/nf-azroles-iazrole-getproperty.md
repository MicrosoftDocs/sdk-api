---
UID: NF:azroles.IAzRole.GetProperty
title: IAzRole::GetProperty
author: windows-driver-content
description: Returns the IAzRole object property with the specified property ID.
old-location: security\iazrole_getproperty.htm
old-project: SecAuthZ
ms.assetid: f65058ce-962d-4cad-9f55-c8b983ffaa05
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AZ_PROP_APPLICATION_DATA, AZ_PROP_CHILD_CREATE, AZ_PROP_DESCRIPTION, AZ_PROP_NAME, AZ_PROP_ROLE_APP_MEMBERS, AZ_PROP_ROLE_MEMBERS, AZ_PROP_ROLE_MEMBERS_NAME, AZ_PROP_ROLE_OPERATIONS, AZ_PROP_ROLE_TASKS, AZ_PROP_WRITABLE, AzRole object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzRole object, GetProperty method [Security],IAzRole interface, IAzRole interface [Security],GetProperty method, IAzRole.GetProperty, IAzRole::GetProperty, azroles/IAzRole::GetProperty, security.iazrole_getproperty
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
-	IAzRole.GetProperty
-	AzRole.GetProperty
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzRole::GetProperty


## -description


The <b>GetProperty</b> method returns the <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object property  with the specified property ID.


## -parameters




### -param lPropId [in]

Property ID of the <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object property  to return. The following table shows the possible values.

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
Also  accessed through the <a href="https://msdn.microsoft.com/6cb85528-35b4-4fed-98bb-6209dd0af0fd">ApplicationData</a>  property

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
Also  accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_APP_MEMBERS"></a><a id="az_prop_role_app_members"></a><dl>
<dt><b>AZ_PROP_ROLE_APP_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/c41933d4-d3fe-485c-9249-e82d51c0bfc9">AppMembers</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_MEMBERS"></a><a id="az_prop_role_members"></a><dl>
<dt><b>AZ_PROP_ROLE_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/03391842-fc8a-4dc2-878e-4fe1c41cc4dd">Members</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_MEMBERS_NAME"></a><a id="az_prop_role_members_name"></a><dl>
<dt><b>AZ_PROP_ROLE_MEMBERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/defaefa8-2d76-49c6-bd1c-8b386f9dc5f1">MembersName</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_OPERATIONS"></a><a id="az_prop_role_operations"></a><dl>
<dt><b>AZ_PROP_ROLE_OPERATIONS</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/44d90f1e-6112-4f02-b840-2ba7af8d9f33">Operations</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_ROLE_TASKS"></a><a id="az_prop_role_tasks"></a><dl>
<dt><b>AZ_PROP_ROLE_TASKS</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/60342e8f-1947-4949-b25e-01db473712ac">Tasks</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_WRITABLE"></a><a id="az_prop_writable"></a><dl>
<dt><b>AZ_PROP_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/053b0ec4-143b-449d-bbbd-8ec8f00b0f2e">Writable</a>  property

</td>
</tr>
</table>
 


### -param varReserved [in, optional]

Reserved for future use.


### -param pvarProp [out]

A pointer to the returned <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object property.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.



