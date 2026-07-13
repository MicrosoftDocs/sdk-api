---
UID: NS:ntsecapi._KERB_QUERY_TKT_CACHE_REQUEST
title: KERB_QUERY_TKT_CACHE_REQUEST (ntsecapi.h)
description: Contains information used to query the ticket cache.
helpviewer_keywords: ["*PKERB_QUERY_TKT_CACHE_REQUEST","KERB_QUERY_TKT_CACHE_REQUEST","KERB_QUERY_TKT_CACHE_REQUEST structure [Security]","PKERB_QUERY_TKT_CACHE_REQUEST","PKERB_QUERY_TKT_CACHE_REQUEST structure pointer [Security]","_lsa_kerb_query_tkt_cache_request","ntsecapi/KERB_QUERY_TKT_CACHE_REQUEST","ntsecapi/PKERB_QUERY_TKT_CACHE_REQUEST","security.kerb_query_tkt_cache_request"]
old-location: security\kerb_query_tkt_cache_request.htm
tech.root: security
ms.assetid: 3c8e63b3-9ac4-4228-87e1-6802c3d12d6c
ms.date: 12/05/2018
ms.keywords: '*PKERB_QUERY_TKT_CACHE_REQUEST, KERB_QUERY_TKT_CACHE_REQUEST, KERB_QUERY_TKT_CACHE_REQUEST structure [Security], PKERB_QUERY_TKT_CACHE_REQUEST, PKERB_QUERY_TKT_CACHE_REQUEST structure pointer [Security], _lsa_kerb_query_tkt_cache_request, ntsecapi/KERB_QUERY_TKT_CACHE_REQUEST, ntsecapi/PKERB_QUERY_TKT_CACHE_REQUEST, security.kerb_query_tkt_cache_request'
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
req.typenames: KERB_QUERY_TKT_CACHE_REQUEST, *PKERB_QUERY_TKT_CACHE_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_QUERY_TKT_CACHE_REQUEST
 - ntsecapi/_KERB_QUERY_TKT_CACHE_REQUEST
 - PKERB_QUERY_TKT_CACHE_REQUEST
 - ntsecapi/PKERB_QUERY_TKT_CACHE_REQUEST
 - KERB_QUERY_TKT_CACHE_REQUEST
 - ntsecapi/KERB_QUERY_TKT_CACHE_REQUEST
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
 - KERB_QUERY_TKT_CACHE_REQUEST
---

# KERB_QUERY_TKT_CACHE_REQUEST structure


## -description

The <b>KERB_QUERY_TKT_CACHE_REQUEST</b> structure contains information used to query the ticket cache.

It is used by 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>.

## -struct-fields

### -field MessageType

<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_protocol_message_type">KERB_PROTOCOL_MESSAGE_TYPE</a> value identifying the type of request being made. This member must be set to <b>KerbQueryTicketCacheMessage</b> or <b>KerbRetrieveTicketMessage</b>. 




If this member is set to <b>KerbQueryTicketCacheMessage</b>, the request is for information about all of the cached tickets for the specified user logon session. If it is set to <b>KerbRetrieveTicketMessage</b>, the request is for the ticket granting ticket from the ticket cache of the specified user logon session.

### -field LogonId

<a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a> structure containing the <a href="/windows/win32/SecGloss/l-gly">logon session</a> identifier. This can be zero for the current user's logon session. If not zero, the caller must have the SeTcbPrivilege privilege set. If this fails, the <a href="/windows/win32/SecGloss/k-gly">Kerberos</a> authentication package sets the <i>ProtocolStatus</i> parameter of <a href="/windows/win32/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> to **STATUS_PRIVILEGE_NOT_HELD**.
