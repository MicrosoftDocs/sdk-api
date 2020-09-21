---
UID: NS:ntsecapi._KERB_PURGE_TKT_CACHE_REQUEST
title: KERB_PURGE_TKT_CACHE_REQUEST (ntsecapi.h)
description: Contains information used to delete entries from the ticket cache.
helpviewer_keywords: ["*PKERB_PURGE_TKT_CACHE_REQUEST","KERB_PURGE_TKT_CACHE_REQUEST","KERB_PURGE_TKT_CACHE_REQUEST structure [Security]","PKERB_PURGE_TKT_CACHE_REQUEST","PKERB_PURGE_TKT_CACHE_REQUEST structure pointer [Security]","_lsa_kerb_purge_tkt_cache_request","ntsecapi/KERB_PURGE_TKT_CACHE_REQUEST","ntsecapi/PKERB_PURGE_TKT_CACHE_REQUEST","security.kerb_purge_tkt_cache_request"]
old-location: security\kerb_purge_tkt_cache_request.htm
tech.root: security
ms.assetid: 4e5e944a-8163-42de-b534-3b0478d9f334
ms.date: 12/05/2018
ms.keywords: '*PKERB_PURGE_TKT_CACHE_REQUEST, KERB_PURGE_TKT_CACHE_REQUEST, KERB_PURGE_TKT_CACHE_REQUEST structure [Security], PKERB_PURGE_TKT_CACHE_REQUEST, PKERB_PURGE_TKT_CACHE_REQUEST structure pointer [Security], _lsa_kerb_purge_tkt_cache_request, ntsecapi/KERB_PURGE_TKT_CACHE_REQUEST, ntsecapi/PKERB_PURGE_TKT_CACHE_REQUEST, security.kerb_purge_tkt_cache_request'
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: KERB_PURGE_TKT_CACHE_REQUEST, *PKERB_PURGE_TKT_CACHE_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_PURGE_TKT_CACHE_REQUEST
 - ntsecapi/_KERB_PURGE_TKT_CACHE_REQUEST
 - PKERB_PURGE_TKT_CACHE_REQUEST
 - ntsecapi/PKERB_PURGE_TKT_CACHE_REQUEST
 - KERB_PURGE_TKT_CACHE_REQUEST
 - ntsecapi/KERB_PURGE_TKT_CACHE_REQUEST
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
 - KERB_PURGE_TKT_CACHE_REQUEST
---

# KERB_PURGE_TKT_CACHE_REQUEST structure


## -description

The <b>KERB_PURGE_TKT_CACHE_REQUEST</b> structure contains information used to delete entries from the ticket cache.

It is used by 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>.

## -struct-fields

### -field MessageType

<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_protocol_message_type">KERB_PROTOCOL_MESSAGE_TYPE</a> value identifying the type of request being made. This member must be set to <b>KerbPurgeTicketCacheMessage</b>.

### -field LogonId

<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> structure containing the <a href="/windows/desktop/SecGloss/l-gly">logon session</a> identifier. This can be zero for the current user's logon session. If not zero, the caller must have the SeTcbPrivilege privilege set. If this fails, the <a href="/windows/desktop/SecGloss/k-gly">Kerberos</a> authentication package sets the <i>ProtocolStatus</i> parameter of <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> to <b>STATUS_ACCESS_DENIED</b>.

### -field ServerName

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the name of the service whose tickets should be deleted from the cache.

### -field RealmName

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the name of the realm whose tickets should be deleted from the cache.

## -remarks

If both <b>ServerName</b> and <b>RealmName</b> are of zero length, <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> will delete all tickets for the logon session identified by <b>LogonId</b>. Otherwise, <b>LsaCallAuthenticationPackage</b> will search the cache tickets for <b>ServerName</b>@<b>RealmName</b>, and will delete all such tickets.


<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> does not return this buffer. It returns STATUS_SUCCESS if one or more tickets are deleted. If no tickets are found, the function returns SEC_E_NO_CREDENTIALS.