---
UID: NS:ntsecapi._KERB_TICKET_UNLOCK_LOGON
title: KERB_TICKET_UNLOCK_LOGON (ntsecapi.h)
description: Contains information to unlock a workstation.
helpviewer_keywords: ["*PKERB_TICKET_UNLOCK_LOGON","KERB_TICKET_UNLOCK_LOGON","KERB_TICKET_UNLOCK_LOGON structure [Security]","PKERB_TICKET_UNLOCK_LOGON","PKERB_TICKET_UNLOCK_LOGON structure pointer [Security]","_lsa_kerb_ticket_unlock_logon","ntsecapi/KERB_TICKET_UNLOCK_LOGON","ntsecapi/PKERB_TICKET_UNLOCK_LOGON","security.kerb_ticket_unlock_logon"]
old-location: security\kerb_ticket_unlock_logon.htm
tech.root: security
ms.assetid: 24daa3d1-1116-4b0b-a19b-a23075a69197
ms.date: 12/05/2018
ms.keywords: '*PKERB_TICKET_UNLOCK_LOGON, KERB_TICKET_UNLOCK_LOGON, KERB_TICKET_UNLOCK_LOGON structure [Security], PKERB_TICKET_UNLOCK_LOGON, PKERB_TICKET_UNLOCK_LOGON structure pointer [Security], _lsa_kerb_ticket_unlock_logon, ntsecapi/KERB_TICKET_UNLOCK_LOGON, ntsecapi/PKERB_TICKET_UNLOCK_LOGON, security.kerb_ticket_unlock_logon'
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
req.typenames: KERB_TICKET_UNLOCK_LOGON, *PKERB_TICKET_UNLOCK_LOGON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_TICKET_UNLOCK_LOGON
 - ntsecapi/_KERB_TICKET_UNLOCK_LOGON
 - PKERB_TICKET_UNLOCK_LOGON
 - ntsecapi/PKERB_TICKET_UNLOCK_LOGON
 - KERB_TICKET_UNLOCK_LOGON
 - ntsecapi/KERB_TICKET_UNLOCK_LOGON
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
 - KERB_TICKET_UNLOCK_LOGON
---

# KERB_TICKET_UNLOCK_LOGON structure


## -description

The <b>KERB_TICKET_UNLOCK_LOGON</b> structure contains information to unlock a workstation.

It is used by 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>.

## -struct-fields

### -field Logon

<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_ticket_logon">KERB_TICKET_LOGON</a> structure. All members of the structure must be the same as the structure used in the original logon except the <a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_logon_submit_type">KERB_LOGON_SUBMIT_TYPE</a> member, which must be set to <b>KerbTicketUnlockLogon</b>.

### -field LogonId

<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> structure containing the logon identifier of the current <a href="/windows/desktop/SecGloss/l-gly">logon session</a>. This ID was previously returned from the initial logon by 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>.