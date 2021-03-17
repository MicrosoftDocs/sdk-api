---
UID: NS:ntsecapi._KERB_TICKET_PROFILE
title: KERB_TICKET_PROFILE (ntsecapi.h)
description: The KERB_TICKET_PROFILE structure contains information about an interactive logon profile. This structure is returned by LsaLogonUser.
helpviewer_keywords: ["*PKERB_TICKET_PROFILE","KERB_TICKET_PROFILE","KERB_TICKET_PROFILE structure [Security]","PKERB_TICKET_PROFILE","PKERB_TICKET_PROFILE structure pointer [Security]","_lsa_kerb_ticket_profile","ntsecapi/KERB_TICKET_PROFILE","ntsecapi/PKERB_TICKET_PROFILE","security.kerb_ticket_profile"]
old-location: security\kerb_ticket_profile.htm
tech.root: security
ms.assetid: 9db0f9ac-b469-4e62-a735-ca3c56086009
ms.date: 12/05/2018
ms.keywords: '*PKERB_TICKET_PROFILE, KERB_TICKET_PROFILE, KERB_TICKET_PROFILE structure [Security], PKERB_TICKET_PROFILE, PKERB_TICKET_PROFILE structure pointer [Security], _lsa_kerb_ticket_profile, ntsecapi/KERB_TICKET_PROFILE, ntsecapi/PKERB_TICKET_PROFILE, security.kerb_ticket_profile'
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
req.typenames: KERB_TICKET_PROFILE, *PKERB_TICKET_PROFILE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_TICKET_PROFILE
 - ntsecapi/_KERB_TICKET_PROFILE
 - PKERB_TICKET_PROFILE
 - ntsecapi/PKERB_TICKET_PROFILE
 - KERB_TICKET_PROFILE
 - ntsecapi/KERB_TICKET_PROFILE
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
 - KERB_TICKET_PROFILE
---

# KERB_TICKET_PROFILE structure


## -description

The <b>KERB_TICKET_PROFILE</b> structure contains information about an interactive logon profile.
			

This structure is returned by 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>.

## -struct-fields

### -field Profile

<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_interactive_profile">KERB_INTERACTIVE_PROFILE</a> structure containing logon information.

### -field SessionKey

<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_crypto_key">KERB_CRYPTO_KEY</a> structure containing the <a href="/windows/desktop/SecGloss/s-gly">session key</a> for the Kerberos ticket.