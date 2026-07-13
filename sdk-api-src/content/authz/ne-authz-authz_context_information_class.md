---
UID: NE:authz._AUTHZ_CONTEXT_INFORMATION_CLASS
title: AUTHZ_CONTEXT_INFORMATION_CLASS (authz.h)
description: Specifies the type of information to be retrieved from an existing AuthzClientContext. This enumeration is used by the AuthzGetInformationFromContext function.
helpviewer_keywords: ["AUTHZ_CONTEXT_INFORMATION_CLASS","AUTHZ_CONTEXT_INFORMATION_CLASS enumeration [Security]","AuthzContextInfoAll","AuthzContextInfoAppContainerSid","AuthzContextInfoAuthenticationId","AuthzContextInfoCapabilitySids","AuthzContextInfoDeviceClaims","AuthzContextInfoDeviceSids","AuthzContextInfoExpirationTime","AuthzContextInfoGroupsSids","AuthzContextInfoIdentifier","AuthzContextInfoPrivileges","AuthzContextInfoRestrictedSids","AuthzContextInfoSecurityAttributes","AuthzContextInfoServerContext","AuthzContextInfoSource","AuthzContextInfoUserClaims","AuthzContextInfoUserSid","_win32_authz_context_information_class_str","authz/AUTHZ_CONTEXT_INFORMATION_CLASS","authz/AuthzContextInfoAll","authz/AuthzContextInfoAppContainerSid","authz/AuthzContextInfoAuthenticationId","authz/AuthzContextInfoCapabilitySids","authz/AuthzContextInfoDeviceClaims","authz/AuthzContextInfoDeviceSids","authz/AuthzContextInfoExpirationTime","authz/AuthzContextInfoGroupsSids","authz/AuthzContextInfoIdentifier","authz/AuthzContextInfoPrivileges","authz/AuthzContextInfoRestrictedSids","authz/AuthzContextInfoSecurityAttributes","authz/AuthzContextInfoServerContext","authz/AuthzContextInfoSource","authz/AuthzContextInfoUserClaims","authz/AuthzContextInfoUserSid","security.authz_context_information_class"]
old-location: security\authz_context_information_class.htm
tech.root: security
ms.assetid: 5eb752dc-17f7-4510-8aef-d18280322e76
ms.date: 12/05/2018
ms.keywords: AUTHZ_CONTEXT_INFORMATION_CLASS, AUTHZ_CONTEXT_INFORMATION_CLASS enumeration [Security], AuthzContextInfoAll, AuthzContextInfoAppContainerSid, AuthzContextInfoAuthenticationId, AuthzContextInfoCapabilitySids, AuthzContextInfoDeviceClaims, AuthzContextInfoDeviceSids, AuthzContextInfoExpirationTime, AuthzContextInfoGroupsSids, AuthzContextInfoIdentifier, AuthzContextInfoPrivileges, AuthzContextInfoRestrictedSids, AuthzContextInfoSecurityAttributes, AuthzContextInfoServerContext, AuthzContextInfoSource, AuthzContextInfoUserClaims, AuthzContextInfoUserSid, _win32_authz_context_information_class_str, authz/AUTHZ_CONTEXT_INFORMATION_CLASS, authz/AuthzContextInfoAll, authz/AuthzContextInfoAppContainerSid, authz/AuthzContextInfoAuthenticationId, authz/AuthzContextInfoCapabilitySids, authz/AuthzContextInfoDeviceClaims, authz/AuthzContextInfoDeviceSids, authz/AuthzContextInfoExpirationTime, authz/AuthzContextInfoGroupsSids, authz/AuthzContextInfoIdentifier, authz/AuthzContextInfoPrivileges, authz/AuthzContextInfoRestrictedSids, authz/AuthzContextInfoSecurityAttributes, authz/AuthzContextInfoServerContext, authz/AuthzContextInfoSource, authz/AuthzContextInfoUserClaims, authz/AuthzContextInfoUserSid, security.authz_context_information_class
req.header: authz.h
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
req.typenames: AUTHZ_CONTEXT_INFORMATION_CLASS
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - _AUTHZ_CONTEXT_INFORMATION_CLASS
 - authz/_AUTHZ_CONTEXT_INFORMATION_CLASS
 - AUTHZ_CONTEXT_INFORMATION_CLASS
 - authz/AUTHZ_CONTEXT_INFORMATION_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Authz.h
api_name:
 - AUTHZ_CONTEXT_INFORMATION_CLASS
---

# AUTHZ_CONTEXT_INFORMATION_CLASS enumeration


## -description

The <b>AUTHZ_CONTEXT_INFORMATION_CLASS</b> enumeration specifies the type of information to be retrieved from an existing AuthzClientContext. This enumeration is used by the  <a href="/windows/desktop/api/authz/nf-authz-authzgetinformationfromcontext">AuthzGetInformationFromContext</a> function.

## -enum-fields

### -field AuthzContextInfoUserSid:1

Retrieves a <a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a> structure that contains a user <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) and its attribute.

### -field AuthzContextInfoGroupsSids

Retrieves a <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that contains the group SIDs to which the user belongs and their attributes.

### -field AuthzContextInfoRestrictedSids

Retrieves a <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that contains the restricted group SIDs in the context and their attributes.

### -field AuthzContextInfoPrivileges

Retrieves a <a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a> structure that contains the privileges held by the user.

### -field AuthzContextInfoExpirationTime

Retrieves the expiration time set on the context.

### -field AuthzContextInfoServerContext

This constant is reserved. Do not use it.

### -field AuthzContextInfoIdentifier

Retrieves an <a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> structures used by the resource manager to identify the context.

### -field AuthzContextInfoSource

This constant is reserved. Do not use it.

### -field AuthzContextInfoAll

This constant is reserved. Do not use it.

### -field AuthzContextInfoAuthenticationId

This constant is reserved. Do not use it.

### -field AuthzContextInfoSecurityAttributes

Retrieves an <a href="/windows/desktop/api/authz/ns-authz-authz_security_attributes_information">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure that contains security attributes.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

### -field AuthzContextInfoDeviceSids

Retrieves a <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that contains device SIDs and their attributes.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

### -field AuthzContextInfoUserClaims

Retrieves a <a href="/windows/desktop/api/authz/ns-authz-authz_security_attributes_information">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure that contains user claims.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

### -field AuthzContextInfoDeviceClaims

Retrieves a <a href="/windows/desktop/api/authz/ns-authz-authz_security_attributes_information">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure that contains device claims.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

### -field AuthzContextInfoAppContainerSid

Retrieves a <a href="/windows/desktop/api/winnt/ns-winnt-token_appcontainer_information">TOKEN_APPCONTAINER_INFORMATION</a> structure that contains the app container SID.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

### -field AuthzContextInfoCapabilitySids

Retrieves a <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that contains capability SIDs.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-enumerations">Authorization Enumerations</a>



<a href="/windows/desktop/api/authz/nf-authz-authzgetinformationfromcontext">AuthzGetInformationFromContext</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_capabilities">SECURITY_CAPABILITIES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_appcontainer_information">TOKEN_APPCONTAINER_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_device_claims">TOKEN_DEVICE_CLAIMS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user_claims">TOKEN_USER_CLAIMS</a>
