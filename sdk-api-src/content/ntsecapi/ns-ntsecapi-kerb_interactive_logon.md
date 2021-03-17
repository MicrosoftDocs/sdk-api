---
UID: NS:ntsecapi._KERB_INTERACTIVE_LOGON
title: KERB_INTERACTIVE_LOGON (ntsecapi.h)
description: Contains information about an interactive logon session.
helpviewer_keywords: ["*PKERB_INTERACTIVE_LOGON","KERB_INTERACTIVE_LOGON","KERB_INTERACTIVE_LOGON structure [Security]","PKERB_INTERACTIVE_LOGON","PKERB_INTERACTIVE_LOGON structure pointer [Security]","_lsa_kerb_interactive_logon","ntsecapi/KERB_INTERACTIVE_LOGON","ntsecapi/PKERB_INTERACTIVE_LOGON","security.kerb_interactive_logon"]
old-location: security\kerb_interactive_logon.htm
tech.root: security
ms.assetid: 96aec0cc-b3e1-4b4b-aa0e-ecf05b9fabbe
ms.date: 12/05/2018
ms.keywords: '*PKERB_INTERACTIVE_LOGON, KERB_INTERACTIVE_LOGON, KERB_INTERACTIVE_LOGON structure [Security], PKERB_INTERACTIVE_LOGON, PKERB_INTERACTIVE_LOGON structure pointer [Security], _lsa_kerb_interactive_logon, ntsecapi/KERB_INTERACTIVE_LOGON, ntsecapi/PKERB_INTERACTIVE_LOGON, security.kerb_interactive_logon'
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
req.typenames: KERB_INTERACTIVE_LOGON, *PKERB_INTERACTIVE_LOGON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_INTERACTIVE_LOGON
 - ntsecapi/_KERB_INTERACTIVE_LOGON
 - PKERB_INTERACTIVE_LOGON
 - ntsecapi/PKERB_INTERACTIVE_LOGON
 - KERB_INTERACTIVE_LOGON
 - ntsecapi/KERB_INTERACTIVE_LOGON
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
 - KERB_INTERACTIVE_LOGON
---

# KERB_INTERACTIVE_LOGON structure


## -description

The <b>KERB_INTERACTIVE_LOGON</b> structure contains information about an interactive <a href="/windows/desktop/SecGloss/l-gly">logon session</a>.

It is used by 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> with the Kerberos security package using LOGON32_PROVIDER_WINNT50 or LOGON32_PROVIDER_DEFAULT.

## -struct-fields

### -field MessageType

<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_logon_submit_type">KERB_LOGON_SUBMIT_TYPE</a> value identifying the type of logon request being made. This member must be set to <b>KerbInteractiveLogon</b>.

### -field LogonDomainName

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> specifying the name of the target logon domain.

### -field UserName

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> specifying the user name.

### -field Password

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> specifying the user password. When you have finished using the password, remove the sensitive information from memory by calling <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a>. For more information on protecting the password, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.