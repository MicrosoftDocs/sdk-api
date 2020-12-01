---
UID: NS:ntsecapi._KERB_RETRIEVE_TKT_RESPONSE
title: KERB_RETRIEVE_TKT_RESPONSE (ntsecapi.h)
description: Contains the response from retrieving a ticket.
helpviewer_keywords: ["*PKERB_RETRIEVE_TKT_RESPONSE","KERB_RETRIEVE_TKT_RESPONSE","KERB_RETRIEVE_TKT_RESPONSE structure [Security]","PKERB_RETRIEVE_TKT_RESPONSE","PKERB_RETRIEVE_TKT_RESPONSE structure pointer [Security]","_lsa_kerb_retrieve_tkt_response","ntsecapi/KERB_RETRIEVE_TKT_RESPONSE","ntsecapi/PKERB_RETRIEVE_TKT_RESPONSE","security.kerb_retrieve_tkt_response"]
old-location: security\kerb_retrieve_tkt_response.htm
tech.root: security
ms.assetid: 682d4076-dc65-4291-8a82-981f207ae432
ms.date: 12/05/2018
ms.keywords: '*PKERB_RETRIEVE_TKT_RESPONSE, KERB_RETRIEVE_TKT_RESPONSE, KERB_RETRIEVE_TKT_RESPONSE structure [Security], PKERB_RETRIEVE_TKT_RESPONSE, PKERB_RETRIEVE_TKT_RESPONSE structure pointer [Security], _lsa_kerb_retrieve_tkt_response, ntsecapi/KERB_RETRIEVE_TKT_RESPONSE, ntsecapi/PKERB_RETRIEVE_TKT_RESPONSE, security.kerb_retrieve_tkt_response'
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
req.typenames: KERB_RETRIEVE_TKT_RESPONSE, *PKERB_RETRIEVE_TKT_RESPONSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_RETRIEVE_TKT_RESPONSE
 - ntsecapi/_KERB_RETRIEVE_TKT_RESPONSE
 - PKERB_RETRIEVE_TKT_RESPONSE
 - ntsecapi/PKERB_RETRIEVE_TKT_RESPONSE
 - KERB_RETRIEVE_TKT_RESPONSE
 - ntsecapi/KERB_RETRIEVE_TKT_RESPONSE
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
 - KERB_RETRIEVE_TKT_RESPONSE
---

# KERB_RETRIEVE_TKT_RESPONSE structure


## -description

The <b>KERB_RETRIEVE_TKT_RESPONSE</b> structure contains the response from retrieving a ticket.

It is used by 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>.

## -struct-fields

### -field Ticket

<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_external_ticket">KERB_EXTERNAL_TICKET</a> structure containing the requested ticket.