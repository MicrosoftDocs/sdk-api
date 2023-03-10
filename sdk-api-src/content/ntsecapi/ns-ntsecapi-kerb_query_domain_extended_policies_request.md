---
UID: NS:ntsecapi._KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST
title: KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST (ntsecapi.h)
description: Contains information used to query the domain for the extended policies.
helpviewer_keywords: ["*PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST","KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST","KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST structure [Security]","PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST","PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST structure pointer [Security]","ntsecapi/KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST","ntsecapi/PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST","security.kerb_query_domain_extended_policies_request"]
old-location: security\kerb_query_domain_extended_policies_request.htm
tech.root: security
ms.assetid: 3900428B-B7FE-4169-BFF0-B8BEEEB342ED
ms.date: 12/05/2018
ms.keywords: '*PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST, KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST, KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST structure [Security], PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST, PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST structure pointer [Security], ntsecapi/KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST, ntsecapi/PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST, security.kerb_query_domain_extended_policies_request'
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
req.typenames: KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST, *PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST
 - ntsecapi/_KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST
 - PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST
 - ntsecapi/PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST
 - KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST
 - ntsecapi/KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST
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
 - KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST
---

# KERB_QUERY_DOMAIN_EXTENDED_POLICIES_REQUEST structure


## -description

Contains information used to query the domain for the extended policies. You must have the <b>SeTcbPrivilege</b> privilege set.

## -struct-fields

### -field MessageType

A 
						value of the <a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_protocol_message_type">KERB_PROTOCOL_MESSAGE_TYPE</a> enumeration that lists the types of messages that can be sent to the <a href="/windows/desktop/SecGloss/k-gly">Kerberos</a> authentication package by calling 
the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function. This member must be set to <b>KerbQueryDomainExtendedPoliciesMessage</b>.

### -field Flags

Reserved.

### -field DomainName

The 	name of the domain that you are querying for the extended policies.