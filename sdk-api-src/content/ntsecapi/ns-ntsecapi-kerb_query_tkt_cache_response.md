---
UID: NS:ntsecapi._KERB_QUERY_TKT_CACHE_RESPONSE
title: KERB_QUERY_TKT_CACHE_RESPONSE (ntsecapi.h)
description: Contains the results of querying the ticket cache.
helpviewer_keywords: ["*PKERB_QUERY_TKT_CACHE_RESPONSE","KERB_QUERY_TKT_CACHE_RESPONSE","KERB_QUERY_TKT_CACHE_RESPONSE structure [Security]","PKERB_QUERY_TKT_CACHE_RESPONSE","PKERB_QUERY_TKT_CACHE_RESPONSE structure pointer [Security]","_lsa_kerb_query_tkt_cache_response","ntsecapi/KERB_QUERY_TKT_CACHE_RESPONSE","ntsecapi/PKERB_QUERY_TKT_CACHE_RESPONSE","security.kerb_query_tkt_cache_response"]
old-location: security\kerb_query_tkt_cache_response.htm
tech.root: security
ms.assetid: 2101c1de-f304-4d44-899f-f9f03cd50934
ms.date: 12/05/2018
ms.keywords: '*PKERB_QUERY_TKT_CACHE_RESPONSE, KERB_QUERY_TKT_CACHE_RESPONSE, KERB_QUERY_TKT_CACHE_RESPONSE structure [Security], PKERB_QUERY_TKT_CACHE_RESPONSE, PKERB_QUERY_TKT_CACHE_RESPONSE structure pointer [Security], _lsa_kerb_query_tkt_cache_response, ntsecapi/KERB_QUERY_TKT_CACHE_RESPONSE, ntsecapi/PKERB_QUERY_TKT_CACHE_RESPONSE, security.kerb_query_tkt_cache_response'
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
req.typenames: KERB_QUERY_TKT_CACHE_RESPONSE, *PKERB_QUERY_TKT_CACHE_RESPONSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_QUERY_TKT_CACHE_RESPONSE
 - ntsecapi/_KERB_QUERY_TKT_CACHE_RESPONSE
 - PKERB_QUERY_TKT_CACHE_RESPONSE
 - ntsecapi/PKERB_QUERY_TKT_CACHE_RESPONSE
 - KERB_QUERY_TKT_CACHE_RESPONSE
 - ntsecapi/KERB_QUERY_TKT_CACHE_RESPONSE
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
 - KERB_QUERY_TKT_CACHE_RESPONSE
---

# KERB_QUERY_TKT_CACHE_RESPONSE structure


## -description

The <b>KERB_QUERY_TKT_CACHE_RESPONSE</b> structure contains the results of querying the ticket cache.

It is used by 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>.

## -struct-fields

### -field MessageType

<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_protocol_message_type">KERB_PROTOCOL_MESSAGE_TYPE</a> value identifying the type of request being made. This member must be set to <b>KerbQueryTicketCacheMessage</b>.

### -field CountOfTickets

Number of tickets in <b>Tickets</b> array. This can be zero if no tickets are available for the specified logon session.

### -field Tickets

Array of length <b>CountOfTickets</b> of 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_ticket_cache_info">KERB_TICKET_CACHE_INFO</a> structures.

## -remarks

This buffer is allocated by the <a href="/windows/desktop/SecGloss/k-gly">Kerberos</a> authentication package and should be deleted by the application that called <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>, using 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreereturnbuffer">LsaFreeReturnBuffer</a>.