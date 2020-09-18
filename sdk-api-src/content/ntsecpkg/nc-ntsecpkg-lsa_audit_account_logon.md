---
UID: NC:ntsecpkg.LSA_AUDIT_ACCOUNT_LOGON
title: LSA_AUDIT_ACCOUNT_LOGON (ntsecpkg.h)
description: The AuditAccountLogon function produces an audit record that represents the mapping of a foreign principal name onto a Windows account.
helpviewer_keywords: ["AuditAccountLogon","AuditAccountLogon callback function [Security]","LSA_AUDIT_ACCOUNT_LOGON","LSA_AUDIT_ACCOUNT_LOGON callback","_ssp_auditaccountlogon","ntsecpkg/AuditAccountLogon","security.auditaccountlogon"]
old-location: security\auditaccountlogon.htm
tech.root: security
ms.assetid: dcf2d16b-8352-4d40-9723-c8cf8465431c
ms.date: 12/05/2018
ms.keywords: AuditAccountLogon, AuditAccountLogon callback function [Security], LSA_AUDIT_ACCOUNT_LOGON, LSA_AUDIT_ACCOUNT_LOGON callback, _ssp_auditaccountlogon, ntsecpkg/AuditAccountLogon, security.auditaccountlogon
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
 - LSA_AUDIT_ACCOUNT_LOGON
 - ntsecpkg/LSA_AUDIT_ACCOUNT_LOGON
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
 - AuditAccountLogon
---

# LSA_AUDIT_ACCOUNT_LOGON callback function


## -description

The <b>AuditAccountLogon</b> function produces an audit record that represents the mapping of a foreign <a href="/windows/desktop/SecGloss/s-gly">principal</a> name onto a Windows account.

## -parameters

### -param AuditId [in]

<a href="/windows/desktop/SecGloss/s-gly">Security package</a>–defined message identifier. This value is included in the audit record.

### -param Success [in]

Specifies whether the audit record is generated on success or failure of the logon.

### -param Source [in]

Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> specifying the source of the logon attempt.

### -param ClientName [in]

Pointer to a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> specifying the client name.

### -param MappedName [in]

Pointer to a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the Windows account name to which the client name was mapped, if any.

### -param Status [in]

An NTSTATUS value specifying any error that occurred.

## -returns

This function returns STATUS_SUCCESS.

## -remarks

A pointer to the <b>AuditAccountLogon</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>