---
UID: NC:ntsecpkg.LSA_AUDIT_LOGON
title: LSA_AUDIT_LOGON (ntsecpkg.h)
description: The AuditLogon function is used to audit a logon attempt.
helpviewer_keywords: ["AuditLogon","AuditLogon callback function [Security]","LSA_AUDIT_LOGON","LSA_AUDIT_LOGON callback","_ssp_auditlogon","ntsecpkg/AuditLogon","security.auditlogon"]
old-location: security\auditlogon.htm
tech.root: security
ms.assetid: 1b0316ae-0c09-4a7e-8443-e59b4db9e825
ms.date: 12/05/2018
ms.keywords: AuditLogon, AuditLogon callback function [Security], LSA_AUDIT_LOGON, LSA_AUDIT_LOGON callback, _ssp_auditlogon, ntsecpkg/AuditLogon, security.auditlogon
req.header: ntsecpkg.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LSA_AUDIT_LOGON
 - ntsecpkg/LSA_AUDIT_LOGON
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - AuditLogon
---

# LSA_AUDIT_LOGON callback function


## -description

The <b>AuditLogon</b> function is used to audit a logon attempt.

## -parameters

### -param Status [in]

Status of the logon attempt.

### -param SubStatus [in]

Additional status information for the logon attempt.

### -param AccountName [in]

Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a>  that contains the account name used in the logon attempt.

### -param AuthenticatingAuthority [in]

Pointer to a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a>  that contains the name of the authority that authenticated the logon, normally the operating system domain name.

### -param WorkstationName [in]

Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a>  that contains the name of the workstation used to attempt the logon.

### -param UserSid [in, optional]

Pointer to the SID of the <a href="/windows/desktop/SecGloss/s-gly">security principal</a> attempting to logon.

### -param LogonType [in]

A 
<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-security_logon_type">SECURITY_LOGON_TYPE</a> value indicating the type of logon.

### -param TokenSource [in]

Pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a> structure  that specifies the source for the user token. This value must include the package name.

### -param LogonId [in]

Pointer to the <a href="/windows/desktop/SecGloss/l-gly">logon session identifier</a>. <i>LogonId</i> is valid only if the logon attempt was successful.

## -remarks

A pointer to the <b>AuditLogon</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>