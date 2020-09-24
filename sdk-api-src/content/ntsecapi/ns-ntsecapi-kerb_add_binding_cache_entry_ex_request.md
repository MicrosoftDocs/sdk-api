---
UID: NS:ntsecapi._KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST
title: KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST (ntsecapi.h)
description: Allows the user to bind to a specific domain controller (DC), overriding the Kerberos domain binding cache.
helpviewer_keywords: ["*PKERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST","DS_INET_ADDRESS","DS_NETBIOS_ADDRESS","KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST","KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST structure [Security]","PKERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST","PKERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST structure pointer [Security]","ntsecapi/KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST","ntsecapi/PKERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST","security.kerb_add_binding_cache_entry_ex_request"]
old-location: security\kerb_add_binding_cache_entry_ex_request.htm
tech.root: security
ms.assetid: B1E58228-59B3-471D-A90C-DAAC17BA7937
ms.date: 12/05/2018
ms.keywords: '*PKERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST, DS_INET_ADDRESS, DS_NETBIOS_ADDRESS, KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST, KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST structure [Security], PKERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST, PKERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST structure pointer [Security], ntsecapi/KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST, ntsecapi/PKERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST, security.kerb_add_binding_cache_entry_ex_request'
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST, *PKERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST
 - ntsecapi/_KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST
 - PKERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST
 - ntsecapi/PKERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST
 - KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST
 - ntsecapi/KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST
---

# KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST structure


## -description

Allows the user to bind to a specific domain controller (DC), overriding the Kerberos domain binding cache. Kerberos enforces a DC lookup when Dynamic Access Control (DAC) is enabled, so typically authentication is not bound to a specific DC. Certain users may want to bind to the specific DC on which they created an account or set a new password to avoid the DC replication delay. You must have the <b>SeTcbPrivilege</b> privilege set.

## -struct-fields

### -field MessageType

A 
						value of the <a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_protocol_message_type">KERB_PROTOCOL_MESSAGE_TYPE</a> enumeration that lists the types of messages that can be sent to the <a href="/windows/desktop/SecGloss/k-gly">Kerberos</a> authentication package by calling 
the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function. This member must be set to <b>KerbAddBindingCacheEntryExMessage</b>.

### -field RealmName

The 	name of the realm of the domain controller.

### -field KdcAddress

The address of the Key Distribution Center (KDC) of the server to  which you want to bind.

### -field AddressType

The type of string that is contained in the <b>KdcAddress</b> member. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DS_INET_ADDRESS"></a><a id="ds_inet_address"></a><dl>
<dt><b>DS_INET_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
The address is a string IP address of the domain controller, for example, "\\157.55.94.74").

</td>
</tr>
<tr>
<td width="40%"><a id="DS_NETBIOS_ADDRESS"></a><a id="ds_netbios_address"></a><dl>
<dt><b>DS_NETBIOS_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
The address is a NetBIOS name of the domain controller, for example, "\\phoenix".

</td>
</tr>
</table>

### -field DcFlags

The domain controller flags that the caller provides. These flags are needed to pass to the <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> function.

## -remarks

To meet both the user's requirements and Kerberos' requirements, you need  to make two calls to override the Kerberos domain binding cache.

<ol>
<li>
First, you construct a request message type of <a href="/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_query_domain_extended_policies_request">KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST</a> in which the <b>MessageType</b> member must be set to <b>KerbQueryDomainExtendedPoliciesMessage</b>. The <b>DomainName</b> member is set to the actual domain name for which the extended domain policies are queried. If <b>DomainName</b> is set to null, the local computer's domain is assumed.

</li>
<li>
Next, you call the <a href="/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_query_domain_extended_policies_response">LsaCallAuthenticationPackage</a> function with Kerberos authentication package and the request message.  Upon successful return, <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_query_domain_extended_policies_response">KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE</a> is returned.<ul>
<li>If the local computer has disabled DAC, the <b>Flags</b> member is set to 	KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE_FLAG_DAC_DISABLED.</li>
<li>If the specified domain has Flexible Authentication Secure Tunneling (FAST) enabled, <b>ExtendedPolicies</b> member is set to  KERB_EXTENDED_POLICY_FAST_CAPABLE (0x10000).</li>
<li>If the specified domain has Claims enabled, <b>ExtendedPolicies</b> member is set to  KERB_EXTENDED_POLICY_CLAIMS_CAPABLE (0x40000).</li>
<li>If the local computer  domain doesn't disable DAC and the specified domain has either FAST or Claims  enabled, the <b>DsFlags</b> member of the <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> function is set to  DS_DIRECTORY_SERVICE_8_REQUIRED. Otherwise, <b>DsFlags</b> is 0.</li>
<li>If the function returns a failure in the <b>ProtocolStatus</b> member, STATUS_NOT_FOUND indicates that the specified domain cannot be queried because the local computer doesn't have trust to the specified domain. Other error codes indicate the actual failure encountered.</li>
</ul>


</li>
<li>
Then you must call <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> with the returned <b>DsFlags</b> set with flags that represent your own requirements, which may be several, so use the  logical operator <b>OR</b>. The <b>DomainControllerInfo</b> member is returned. 

</li>
<li>
Finally, you call the <a href="/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_query_domain_extended_policies_response">LsaCallAuthenticationPackage</a> function again with the Kerberos authentication package and the request <b>KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST</b> in which the <b>DcFlags</b> member is set to the <b>DomainControllerInfo</b> flags. All other members should be populated in the same way as <b>KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST</b>. If the <b>DsFlags</b> of the <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_query_domain_extended_policies_response">KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE</a> is zero, then either <b>DcFlags</b> should be set to zero when calling <b>KERB_ADD_BINDING_CACHE_ENTRY_EX_REQUEST</b> or default back to the existing KERB_ADD_BINDING_CACHE_ENTRY_REQUEST request.

</li>
</ol>

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>