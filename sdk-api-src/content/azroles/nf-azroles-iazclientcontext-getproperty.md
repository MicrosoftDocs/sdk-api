---
UID: NF:azroles.IAzClientContext.GetProperty
title: IAzClientContext::GetProperty
author: windows-sdk-content
description: Returns the IAzClientContext object property with the specified property ID.
old-location: security\iazclientcontext_getproperty.htm
tech.root: SecAuthZ
ms.assetid: 4be02b6d-5eeb-46e6-9339-3edd904f3606
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AZ_PROP_CHILD_CREATE, AZ_PROP_CLIENT_CONTEXT_ROLE_FOR_ACCESS_CHECK, AZ_PROP_CLIENT_CONTEXT_USER_CANONICAL, AZ_PROP_CLIENT_CONTEXT_USER_DISPLAY, AZ_PROP_CLIENT_CONTEXT_USER_DN, AZ_PROP_CLIENT_CONTEXT_USER_DNS_SAM_COMPAT, AZ_PROP_CLIENT_CONTEXT_USER_GUID, AZ_PROP_CLIENT_CONTEXT_USER_SAM_COMPAT, AZ_PROP_CLIENT_CONTEXT_USER_UPN, AzClientContext object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzClientContext object, GetProperty method [Security],IAzClientContext interface, IAzClientContext interface [Security],GetProperty method, IAzClientContext.GetProperty, IAzClientContext::GetProperty, azroles/IAzClientContext::GetProperty, security.iazclientcontext_getproperty
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
 - IAzClientContext.GetProperty
 - AzClientContext.GetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzClientContext::GetProperty


## -description


The <b>GetProperty</b> method returns the <a href="https://msdn.microsoft.com/e24184d2-a77b-4a8b-b2f3-78f1e0b902f9">IAzClientContext</a> object property  with the specified property ID.


## -parameters




### -param lPropId [in]

Property ID of the <a href="https://msdn.microsoft.com/e24184d2-a77b-4a8b-b2f3-78f1e0b902f9">IAzClientContext</a> object property  to return. The following table shows the possible values.

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
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_ROLE_FOR_ACCESS_CHECK"></a><a id="az_prop_client_context_role_for_access_check"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_ROLE_FOR_ACCESS_CHECK</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/817b3693-b989-431c-a8b3-bdeeb0367dc6">RoleForAccessCheck</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_USER_CANONICAL"></a><a id="az_prop_client_context_user_canonical"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_USER_CANONICAL</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/413cdbbd-a9c6-4117-9df5-d7eb202191a4">UserCanonical</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_USER_DISPLAY"></a><a id="az_prop_client_context_user_display"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_USER_DISPLAY</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/db75ecc1-0096-4e14-a5be-10b596ad5163">UserDisplay</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_USER_DN"></a><a id="az_prop_client_context_user_dn"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_USER_DN</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/1561352c-254e-41a2-bfc9-795a678ce180">UserDn</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_USER_DNS_SAM_COMPAT"></a><a id="az_prop_client_context_user_dns_sam_compat"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_USER_DNS_SAM_COMPAT</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/8f2739cd-3add-4a3c-9c00-8b23d2cec068">UserDnsSamCompat</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_USER_GUID"></a><a id="az_prop_client_context_user_guid"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_USER_GUID</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/fd60d1d0-67b9-457f-a01e-6ea470d9db6a">UserGuid</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_USER_SAM_COMPAT"></a><a id="az_prop_client_context_user_sam_compat"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_USER_SAM_COMPAT</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/3b1f9e8a-cc3b-4be6-b2d9-8e8b3164d46a">UserSamCompat</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_USER_UPN"></a><a id="az_prop_client_context_user_upn"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_USER_UPN</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/e54d450b-7059-43c7-9c08-688975031401">UserUpn</a> property

</td>
</tr>
</table>
 


### -param varReserved [in, optional]

Reserved for future use.


### -param pvarProp [out]

A pointer to the returned <a href="https://msdn.microsoft.com/e24184d2-a77b-4a8b-b2f3-78f1e0b902f9">IAzClientContext</a> object property.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.



