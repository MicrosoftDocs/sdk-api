---
UID: NS:ntsecapi._KERB_TICKET_PROFILE
title: KERB_TICKET_PROFILE (ntsecapi.h)

description: The KERB_TICKET_PROFILE structure contains information about an interactive logon profile. This structure is returned by LsaLogonUser.
old-location: security\kerb_ticket_profile.htm
tech.root: SecAuthN
ms.assetid: 9db0f9ac-b469-4e62-a735-ca3c56086009

ms.date: 12/05/2018
ms.keywords: '*PKERB_TICKET_PROFILE, KERB_TICKET_PROFILE, KERB_TICKET_PROFILE structure [Security], PKERB_TICKET_PROFILE, PKERB_TICKET_PROFILE structure pointer [Security], _lsa_kerb_ticket_profile, ntsecapi/KERB_TICKET_PROFILE, ntsecapi/PKERB_TICKET_PROFILE, security.kerb_ticket_profile'
ms.topic: struct
f1_keywords:
- ntsecapi/KERB_TICKET_PROFILE
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Ntsecapi.h
api_name:
- KERB_TICKET_PROFILE
targetos: Windows
req.typenames: KERB_TICKET_PROFILE, *PKERB_TICKET_PROFILE
req.redist: 
ms.custom: 19H1
---

# KERB_TICKET_PROFILE structure


## -description


The <b>KERB_TICKET_PROFILE</b> structure contains information about an interactive logon profile.
			

This structure is returned by 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>.


## -struct-fields




### -field Profile


<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_interactive_profile">KERB_INTERACTIVE_PROFILE</a> structure containing logon information.


### -field SessionKey


<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_crypto_key">KERB_CRYPTO_KEY</a> structure containing the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">session key</a> for the Kerberos ticket.

