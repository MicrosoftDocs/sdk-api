---
UID: NF:azroles.IAzClientContext.GetProperty
title: IAzClientContext::GetProperty (azroles.h)
description: Returns the IAzClientContext object property with the specified property ID.
helpviewer_keywords: ["AZ_PROP_CHILD_CREATE","AZ_PROP_CLIENT_CONTEXT_ROLE_FOR_ACCESS_CHECK","AZ_PROP_CLIENT_CONTEXT_USER_CANONICAL","AZ_PROP_CLIENT_CONTEXT_USER_DISPLAY","AZ_PROP_CLIENT_CONTEXT_USER_DN","AZ_PROP_CLIENT_CONTEXT_USER_DNS_SAM_COMPAT","AZ_PROP_CLIENT_CONTEXT_USER_GUID","AZ_PROP_CLIENT_CONTEXT_USER_SAM_COMPAT","AZ_PROP_CLIENT_CONTEXT_USER_UPN","AzClientContext object [Security]","GetProperty method","GetProperty","GetProperty method [Security]","GetProperty method [Security]","AzClientContext object","GetProperty method [Security]","IAzClientContext interface","IAzClientContext interface [Security]","GetProperty method","IAzClientContext.GetProperty","IAzClientContext::GetProperty","azroles/IAzClientContext::GetProperty","security.iazclientcontext_getproperty"]
old-location: security\iazclientcontext_getproperty.htm
tech.root: security
ms.assetid: 4be02b6d-5eeb-46e6-9339-3edd904f3606
ms.date: 12/05/2018
ms.keywords: AZ_PROP_CHILD_CREATE, AZ_PROP_CLIENT_CONTEXT_ROLE_FOR_ACCESS_CHECK, AZ_PROP_CLIENT_CONTEXT_USER_CANONICAL, AZ_PROP_CLIENT_CONTEXT_USER_DISPLAY, AZ_PROP_CLIENT_CONTEXT_USER_DN, AZ_PROP_CLIENT_CONTEXT_USER_DNS_SAM_COMPAT, AZ_PROP_CLIENT_CONTEXT_USER_GUID, AZ_PROP_CLIENT_CONTEXT_USER_SAM_COMPAT, AZ_PROP_CLIENT_CONTEXT_USER_UPN, AzClientContext object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzClientContext object, GetProperty method [Security],IAzClientContext interface, IAzClientContext interface [Security],GetProperty method, IAzClientContext.GetProperty, IAzClientContext::GetProperty, azroles/IAzClientContext::GetProperty, security.iazclientcontext_getproperty
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
 - IAzClientContext::GetProperty
 - azroles/IAzClientContext::GetProperty
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
 - IAzClientContext.GetProperty
 - AzClientContext.GetProperty
---

# IAzClientContext::GetProperty


## -description

The <b>GetProperty</b> method returns the <a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext">IAzClientContext</a> object property  with the specified property ID.

## -parameters

### -param lPropId [in]

Property ID of the <a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext">IAzClientContext</a> object property  to return. The following table shows the possible values.

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
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck">RoleForAccessCheck</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_USER_CANONICAL"></a><a id="az_prop_client_context_user_canonical"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_USER_CANONICAL</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-get_usercanonical">UserCanonical</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_USER_DISPLAY"></a><a id="az_prop_client_context_user_display"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_USER_DISPLAY</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-get_userdisplay">UserDisplay</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_USER_DN"></a><a id="az_prop_client_context_user_dn"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_USER_DN</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-get_userdn">UserDn</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_USER_DNS_SAM_COMPAT"></a><a id="az_prop_client_context_user_dns_sam_compat"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_USER_DNS_SAM_COMPAT</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-get_userdnssamcompat">UserDnsSamCompat</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_USER_GUID"></a><a id="az_prop_client_context_user_guid"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_USER_GUID</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-get_userguid">UserGuid</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_USER_SAM_COMPAT"></a><a id="az_prop_client_context_user_sam_compat"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_USER_SAM_COMPAT</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-get_usersamcompat">UserSamCompat</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CLIENT_CONTEXT_USER_UPN"></a><a id="az_prop_client_context_user_upn"></a><dl>
<dt><b>AZ_PROP_CLIENT_CONTEXT_USER_UPN</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-get_userupn">UserUpn</a> property

</td>
</tr>
</table>

### -param varReserved [in, optional]

Reserved for future use.

### -param pvarProp [out]

A pointer to the returned <a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext">IAzClientContext</a> object property.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.