---
UID: NS:ntsecapi._KERB_ADD_BINDING_CACHE_ENTRY_REQUEST
title: KERB_ADD_BINDING_CACHE_ENTRY_REQUEST (ntsecapi.h)
description: Specifies a message to add a binding cache entry.
helpviewer_keywords: ["*PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST","DS_INET_ADDRESS","DS_NETBIOS_ADDRESS","KERB_ADD_BINDING_CACHE_ENTRY_REQUEST","KERB_ADD_BINDING_CACHE_ENTRY_REQUEST structure [Security]","PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST","PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST structure pointer [Security]","ntsecapi/KERB_ADD_BINDING_CACHE_ENTRY_REQUEST","ntsecapi/PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST","security.kerb_add_binding_cache_entry_request"]
old-location: security\kerb_add_binding_cache_entry_request.htm
tech.root: security
ms.assetid: 2EFB8F01-0665-4031-B02A-8ECB5B9C7C21
ms.date: 12/05/2018
ms.keywords: '*PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST, DS_INET_ADDRESS, DS_NETBIOS_ADDRESS, KERB_ADD_BINDING_CACHE_ENTRY_REQUEST, KERB_ADD_BINDING_CACHE_ENTRY_REQUEST structure [Security], PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST, PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST structure pointer [Security], ntsecapi/KERB_ADD_BINDING_CACHE_ENTRY_REQUEST, ntsecapi/PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST, security.kerb_add_binding_cache_entry_request'
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: KERB_ADD_BINDING_CACHE_ENTRY_REQUEST, *PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_ADD_BINDING_CACHE_ENTRY_REQUEST
 - ntsecapi/_KERB_ADD_BINDING_CACHE_ENTRY_REQUEST
 - PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST
 - ntsecapi/PKERB_ADD_BINDING_CACHE_ENTRY_REQUEST
 - KERB_ADD_BINDING_CACHE_ENTRY_REQUEST
 - ntsecapi/KERB_ADD_BINDING_CACHE_ENTRY_REQUEST
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
 - KERB_ADD_BINDING_CACHE_ENTRY_REQUEST
---

# KERB_ADD_BINDING_CACHE_ENTRY_REQUEST structure


## -description

Specifies a message to add a binding cache entry. You must have the <b>SeTcbPrivilege</b> privilege set.

## -struct-fields

### -field MessageType

A 
						value of the <a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_protocol_message_type">KERB_PROTOCOL_MESSAGE_TYPE</a> enumeration that lists the types of messages that can be sent to the <a href="/windows/desktop/SecGloss/k-gly">Kerberos</a> authentication package by calling 
the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function. This member must be set to <b>KerbAddBindingCacheEntryMessage</b>.

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