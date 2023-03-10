---
UID: NS:ntsecapi._KERB_SMART_CARD_LOGON
title: KERB_SMART_CARD_LOGON (ntsecapi.h)
description: Contains information about a smart card logon session. (KERB_SMART_CARD_LOGON)
helpviewer_keywords: ["*PKERB_SMART_CARD_LOGON","KERB_SMART_CARD_LOGON","KERB_SMART_CARD_LOGON structure [Security]","PKERB_SMART_CARD_LOGON","PKERB_SMART_CARD_LOGON structure pointer [Security]","ntsecapi/KERB_SMART_CARD_LOGON","ntsecapi/PKERB_SMART_CARD_LOGON","security.kerb_smart_card_logon"]
old-location: security\kerb_smart_card_logon.htm
tech.root: security
ms.assetid: 1a154034-6a2d-46be-9fb6-7c7d425d12f6
ms.date: 12/05/2018
ms.keywords: '*PKERB_SMART_CARD_LOGON, KERB_SMART_CARD_LOGON, KERB_SMART_CARD_LOGON structure [Security], PKERB_SMART_CARD_LOGON, PKERB_SMART_CARD_LOGON structure pointer [Security], ntsecapi/KERB_SMART_CARD_LOGON, ntsecapi/PKERB_SMART_CARD_LOGON, security.kerb_smart_card_logon'
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
req.typenames: KERB_SMART_CARD_LOGON, *PKERB_SMART_CARD_LOGON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_SMART_CARD_LOGON
 - ntsecapi/_KERB_SMART_CARD_LOGON
 - PKERB_SMART_CARD_LOGON
 - ntsecapi/PKERB_SMART_CARD_LOGON
 - KERB_SMART_CARD_LOGON
 - ntsecapi/KERB_SMART_CARD_LOGON
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
 - KERB_SMART_CARD_LOGON
---

# KERB_SMART_CARD_LOGON structure


## -description

The <b>KERB_SMART_CARD_LOGON</b> structure contains information about a smart card <a href="/windows/desktop/SecGloss/l-gly">logon session</a>.

It is used by 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> with the Kerberos security package using LOGON32_PROVIDER_WINNT50 or LOGON32_PROVIDER_DEFAULT.

## -struct-fields

### -field MessageType

<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_logon_submit_type">KERB_LOGON_SUBMIT_TYPE</a> value identifying the type of logon request being made. This member must be set to <b>KerbInteractiveLogon</b>.

### -field Pin

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that specifies the PIN associated with the smart card.

### -field CspDataLength

The length, in characters, of the <b>CspData</b> member.

### -field CspData

A pointer to a <b>KERB_SMARTCARD_CSP_INFO</b> structure that contains information about the smart card cryptographic service provider (CSP) or a pointer to a marshaled <b>KERB_CERTIFICATE_INFO</b> structure when updating certificate credentials.
