---
UID: NF:azroles.IAzScope.GetProperty
title: IAzScope::GetProperty
author: windows-sdk-content
description: Returns the IAzScope object property with the specified property ID.
old-location: security\iazscope_getproperty.htm
tech.root: secauthz
ms.assetid: c3b5b526-5662-4971-8ba2-663e4b2c36ff
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: AZ_PROP_APPLICATION_DATA, AZ_PROP_CHILD_CREATE, AZ_PROP_DESCRIPTION, AZ_PROP_NAME, AZ_PROP_POLICY_ADMINS, AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS, AZ_PROP_POLICY_READERS_NAME, AZ_PROP_SCOPE_BIZRULES_WRITABLE, AZ_PROP_SCOPE_CAN_BE_DELEGATED, AZ_PROP_WRITABLE, AzScope object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzScope object, GetProperty method [Security],IAzScope interface, IAzScope interface [Security],GetProperty method, IAzScope.GetProperty, IAzScope::GetProperty, azroles/IAzScope::GetProperty, security.iazscope_getproperty
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
 - IAzScope.GetProperty
 - AzScope.GetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
- apiref
: 
- COM
: 
- azroles.h
: 
- IAzScope.GetProperty
: 
---

# IAzScope::GetProperty


## -description


The <b>GetProperty</b> method returns the <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object property  with the specified property ID.


## -parameters




### -param lPropId [in]

Property ID of the <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object property  to return. The following table shows the possible values.

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
Also accessed through the <a href="https://msdn.microsoft.com/c54aaadb-0c4a-43f9-ac50-413ed190b365">ApplicationData</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CHILD_CREATE"></a><a id="az_prop_child_create"></a><dl>
<dt><b>AZ_PROP_CHILD_CREATE</b></dt>
</dl>
</td>
<td width="60%">
Determines whether the current user has permission to create child objects. This value is <b>TRUE</b> if the current user has permission; otherwise, <b>FALSE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/51a7daff-ecb9-4a66-a7f7-aee9aeff7d6a">Description</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/66c5722a-5217-4e77-b14f-f9cfa4e030c0">Name</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS"></a><a id="az_prop_policy_admins"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/13c11105-b44d-46e0-ab73-c11fede1507b">PolicyAdministrators</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS_NAME"></a><a id="az_prop_policy_admins_name"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/291aa2f8-f08e-45f5-ade7-b456c962dd3f">PolicyAdministratorsName</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS"></a><a id="az_prop_policy_readers"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/7576997c-a585-4f0d-bec5-c616d39633f9">PolicyReaders</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS_NAME"></a><a id="az_prop_policy_readers_name"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/4f56ee3f-f987-4569-9e19-c13ab3ff100a">PolicyReadersName</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_SCOPE_BIZRULES_WRITABLE"></a><a id="az_prop_scope_bizrules_writable"></a><dl>
<dt><b>AZ_PROP_SCOPE_BIZRULES_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/7cd84e64-ef90-48ca-8da0-88ca6d79e1bf">BizrulesWritable</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_SCOPE_CAN_BE_DELEGATED"></a><a id="az_prop_scope_can_be_delegated"></a><dl>
<dt><b>AZ_PROP_SCOPE_CAN_BE_DELEGATED</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/e68bd5b2-060b-478b-9375-b23761888e6a">CanBeDelegated</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_WRITABLE"></a><a id="az_prop_writable"></a><dl>
<dt><b>AZ_PROP_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/8e382af1-192f-4530-82a0-434f66eac060">Writable</a> property

</td>
</tr>
</table>
 


### -param varReserved [in, optional]

Reserved for future use.


### -param pvarProp [out]

A pointer to the returned <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object property.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.



