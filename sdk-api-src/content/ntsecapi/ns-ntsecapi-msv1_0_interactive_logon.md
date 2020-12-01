---
UID: NS:ntsecapi._MSV1_0_INTERACTIVE_LOGON
title: MSV1_0_INTERACTIVE_LOGON (ntsecapi.h)
description: Contains information about an interactive logon.
helpviewer_keywords: ["*PMSV1_0_INTERACTIVE_LOGON","MSV1_0_INTERACTIVE_LOGON","MSV1_0_INTERACTIVE_LOGON structure [Security]","_lsa_msv1_0_interactive_logon","ntsecapi/MSV1_0_INTERACTIVE_LOGON","security.msv1_0_interactive_logon"]
old-location: security\msv1_0_interactive_logon.htm
tech.root: security
ms.assetid: f9b9a966-54b9-4f89-98cc-d92e3f74571d
ms.date: 12/05/2018
ms.keywords: '*PMSV1_0_INTERACTIVE_LOGON, MSV1_0_INTERACTIVE_LOGON, MSV1_0_INTERACTIVE_LOGON structure [Security], _lsa_msv1_0_interactive_logon, ntsecapi/MSV1_0_INTERACTIVE_LOGON, security.msv1_0_interactive_logon'
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
req.typenames: MSV1_0_INTERACTIVE_LOGON, *PMSV1_0_INTERACTIVE_LOGON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MSV1_0_INTERACTIVE_LOGON
 - ntsecapi/_MSV1_0_INTERACTIVE_LOGON
 - PMSV1_0_INTERACTIVE_LOGON
 - ntsecapi/PMSV1_0_INTERACTIVE_LOGON
 - MSV1_0_INTERACTIVE_LOGON
 - ntsecapi/MSV1_0_INTERACTIVE_LOGON
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
 - MSV1_0_INTERACTIVE_LOGON
---

# MSV1_0_INTERACTIVE_LOGON structure


## -description

The <b>MSV1_0_INTERACTIVE_LOGON</b> structure contains information about an interactive logon.

It is used by the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> function.

## -struct-fields

### -field MessageType

<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-msv1_0_logon_submit_type">MSV1_0_LOGON_SUBMIT_TYPE</a> value that specifies the type of logon being requested. This member must be set to <b>MsV1_0InteractiveLogon</b>.

### -field LogonDomainName

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that contains the name of the logon domain. The specified domain name must be a Windows domain or mixed domain that is trusted by this machine.

The <b>Buffer</b> member of the <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> is relative to the KERB_INTERACTIVE_LOGON structure and must point to memory that is contiguous to the MSV1_0_INTERACTIVE_LOGON structure.

### -field UserName

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that represents the user's account name. The name can be up to 255 bytes long. The name is treated as case-insensitive. The specified <b>UserName</b> must have an account in domain <b>LogonDomainName</b>.

The <b>Buffer</b> member of the <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> is relative to the KERB_INTERACTIVE_LOGON structure and must point to memory that is contiguous to the MSV1_0_INTERACTIVE_LOGON structure.

### -field Password

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that contains the user's <a href="/windows/desktop/SecGloss/p-gly">plaintext</a> password. The password may be up to 255 bytes long and contain any Unicode value. When you have finished using the password, clear it from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information on protecting the password, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

The <b>Buffer</b> member of the <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> is relative to the KERB_INTERACTIVE_LOGON structure and must point to memory that is contiguous to the MSV1_0_INTERACTIVE_LOGON structure.

## -see-also

<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-msv1_0_logon_submit_type">MSV1_0_LOGON_SUBMIT_TYPE</a>