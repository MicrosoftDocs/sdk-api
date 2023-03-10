---
UID: NE:winnt._SECURITY_IMPERSONATION_LEVEL
title: SECURITY_IMPERSONATION_LEVEL (winnt.h)
description: Contains values that specify security impersonation levels. Security impersonation levels govern the degree to which a server process can act on behalf of a client process.
helpviewer_keywords: ["*PSECURITY_IMPERSONATION_LEVEL","PSECURITY_IMPERSONATION_LEVEL","PSECURITY_IMPERSONATION_LEVEL enumeration pointer [Security]","SECURITY_IMPERSONATION_LEVEL","SECURITY_IMPERSONATION_LEVEL enumeration [Security]","SecurityAnonymous","SecurityDelegation","SecurityIdentification","SecurityImpersonation","_win32_security_impersonation_level_str","security.security_impersonation_level","winnt/PSECURITY_IMPERSONATION_LEVEL","winnt/SECURITY_IMPERSONATION_LEVEL","winnt/SecurityAnonymous","winnt/SecurityDelegation","winnt/SecurityIdentification","winnt/SecurityImpersonation"]
old-location: security\security_impersonation_level.htm
tech.root: security
ms.assetid: a75ad777-c88e-4899-be50-0118c113a600
ms.date: 12/05/2018
ms.keywords: '*PSECURITY_IMPERSONATION_LEVEL, PSECURITY_IMPERSONATION_LEVEL, PSECURITY_IMPERSONATION_LEVEL enumeration pointer [Security], SECURITY_IMPERSONATION_LEVEL, SECURITY_IMPERSONATION_LEVEL enumeration [Security], SecurityAnonymous, SecurityDelegation, SecurityIdentification, SecurityImpersonation, _win32_security_impersonation_level_str, security.security_impersonation_level, winnt/PSECURITY_IMPERSONATION_LEVEL, winnt/SECURITY_IMPERSONATION_LEVEL, winnt/SecurityAnonymous, winnt/SecurityDelegation, winnt/SecurityIdentification, winnt/SecurityImpersonation'
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: SECURITY_IMPERSONATION_LEVEL, *PSECURITY_IMPERSONATION_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECURITY_IMPERSONATION_LEVEL
 - winnt/_SECURITY_IMPERSONATION_LEVEL
 - PSECURITY_IMPERSONATION_LEVEL
 - winnt/PSECURITY_IMPERSONATION_LEVEL
 - SECURITY_IMPERSONATION_LEVEL
 - winnt/SECURITY_IMPERSONATION_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - SECURITY_IMPERSONATION_LEVEL
---

# SECURITY_IMPERSONATION_LEVEL enumeration


## -description

The <b>SECURITY_IMPERSONATION_LEVEL</b> enumeration contains values that specify security impersonation levels. Security impersonation levels govern the degree to which a server process can act on behalf of a client <a href="/windows/desktop/SecGloss/p-gly">process</a>.

## -enum-fields

### -field SecurityAnonymous

The server process cannot obtain identification information about the client, and it cannot impersonate the client. It is defined with no value given, and thus, by ANSI C rules, defaults to a value of zero.

### -field SecurityIdentification

The server process can obtain information about the client, such as security identifiers and <a href="/windows/desktop/SecGloss/p-gly">privileges</a>, but it cannot impersonate the client. This is useful for servers that export their own objects, for example, database products that export tables and views. Using the retrieved client-security information, the server can make access-validation decisions without being able to use other services that are using the client's <a href="/windows/desktop/SecGloss/s-gly">security context</a>.

### -field SecurityImpersonation

The server process can impersonate the client's security context on its local system. The server cannot impersonate the client on remote systems.

### -field SecurityDelegation

The server process can impersonate the client's security context on remote systems.

## -remarks

Impersonation is the ability of a process to take on the security attributes of another process.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-enumerations">Authorization Enumerations</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity">CreatePrivateObjectSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex">DuplicateTokenEx</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself">ImpersonateSelf</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a>