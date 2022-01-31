---
UID: NE:winnt._TOKEN_INFORMATION_CLASS
title: TOKEN_INFORMATION_CLASS (winnt.h)
description: Contains values that specify the type of information being assigned to or retrieved from an access token.
helpviewer_keywords: ["*PTOKEN_INFORMATION_CLASS","MaxTokenInfoClass","PTOKEN_INFORMATION_CLASS","PTOKEN_INFORMATION_CLASS enumeration pointer [Security]","TOKEN_INFORMATION_CLASS","TOKEN_INFORMATION_CLASS enumeration [Security]","TokenAccessInformation","TokenAppContainerNumber","TokenAppContainerSid","TokenAuditPolicy","TokenCapabilities","TokenDefaultDacl","TokenDeviceClaimAttributes","TokenDeviceGroups","TokenElevation","TokenElevationType","TokenGroups","TokenGroupsAndPrivileges","TokenHasRestrictions","TokenImpersonationLevel","TokenIntegrityLevel","TokenIsAppContainer","TokenIsRestricted","TokenLinkedToken","TokenLogonSid","TokenMandatoryPolicy","TokenOrigin","TokenOwner","TokenPrimaryGroup","TokenPrivileges","TokenRestrictedDeviceClaimAttributes","TokenRestrictedDeviceGroups","TokenRestrictedSids","TokenRestrictedUserClaimAttributes","TokenSandBoxInert","TokenSecurityAttributes","TokenSessionId","TokenSessionReference","TokenSource","TokenStatistics","TokenType","TokenUIAccess","TokenUser","TokenUserClaimAttributes","TokenVirtualizationAllowed","TokenVirtualizationEnabled","_win32_token_information_class_str","security.token_information_class","winnt/MaxTokenInfoClass","winnt/PTOKEN_INFORMATION_CLASS","winnt/TOKEN_INFORMATION_CLASS","winnt/TokenAccessInformation","winnt/TokenAppContainerNumber","winnt/TokenAppContainerSid","winnt/TokenAuditPolicy","winnt/TokenCapabilities","winnt/TokenDefaultDacl","winnt/TokenDeviceClaimAttributes","winnt/TokenDeviceGroups","winnt/TokenElevation","winnt/TokenElevationType","winnt/TokenGroups","winnt/TokenGroupsAndPrivileges","winnt/TokenHasRestrictions","winnt/TokenImpersonationLevel","winnt/TokenIntegrityLevel","winnt/TokenIsAppContainer","winnt/TokenIsRestricted","winnt/TokenLinkedToken","winnt/TokenLogonSid","winnt/TokenMandatoryPolicy","winnt/TokenOrigin","winnt/TokenOwner","winnt/TokenPrimaryGroup","winnt/TokenPrivileges","winnt/TokenRestrictedDeviceClaimAttributes","winnt/TokenRestrictedDeviceGroups","winnt/TokenRestrictedSids","winnt/TokenRestrictedUserClaimAttributes","winnt/TokenSandBoxInert","winnt/TokenSecurityAttributes","winnt/TokenSessionId","winnt/TokenSessionReference","winnt/TokenSource","winnt/TokenStatistics","winnt/TokenType","winnt/TokenUIAccess","winnt/TokenUser","winnt/TokenUserClaimAttributes","winnt/TokenVirtualizationAllowed","winnt/TokenVirtualizationEnabled"]
old-location: security\token_information_class.htm
tech.root: security
ms.assetid: cb606665-1266-4e71-a145-9b04bf157cdc
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_INFORMATION_CLASS, MaxTokenInfoClass, PTOKEN_INFORMATION_CLASS, PTOKEN_INFORMATION_CLASS enumeration pointer [Security], TOKEN_INFORMATION_CLASS, TOKEN_INFORMATION_CLASS enumeration [Security], TokenAccessInformation, TokenAppContainerNumber, TokenAppContainerSid, TokenAuditPolicy, TokenCapabilities, TokenDefaultDacl, TokenDeviceClaimAttributes, TokenDeviceGroups, TokenElevation, TokenElevationType, TokenGroups, TokenGroupsAndPrivileges, TokenHasRestrictions, TokenImpersonationLevel, TokenIntegrityLevel, TokenIsAppContainer, TokenIsRestricted, TokenLinkedToken, TokenLogonSid, TokenMandatoryPolicy, TokenOrigin, TokenOwner, TokenPrimaryGroup, TokenPrivileges, TokenRestrictedDeviceClaimAttributes, TokenRestrictedDeviceGroups, TokenRestrictedSids, TokenRestrictedUserClaimAttributes, TokenSandBoxInert, TokenSecurityAttributes, TokenSessionId, TokenSessionReference, TokenSource, TokenStatistics, TokenType, TokenUIAccess, TokenUser, TokenUserClaimAttributes, TokenVirtualizationAllowed, TokenVirtualizationEnabled, _win32_token_information_class_str, security.token_information_class, winnt/MaxTokenInfoClass, winnt/PTOKEN_INFORMATION_CLASS, winnt/TOKEN_INFORMATION_CLASS, winnt/TokenAccessInformation, winnt/TokenAppContainerNumber, winnt/TokenAppContainerSid, winnt/TokenAuditPolicy, winnt/TokenCapabilities, winnt/TokenDefaultDacl, winnt/TokenDeviceClaimAttributes, winnt/TokenDeviceGroups, winnt/TokenElevation, winnt/TokenElevationType, winnt/TokenGroups, winnt/TokenGroupsAndPrivileges, winnt/TokenHasRestrictions, winnt/TokenImpersonationLevel, winnt/TokenIntegrityLevel, winnt/TokenIsAppContainer, winnt/TokenIsRestricted, winnt/TokenLinkedToken, winnt/TokenLogonSid, winnt/TokenMandatoryPolicy, winnt/TokenOrigin, winnt/TokenOwner, winnt/TokenPrimaryGroup, winnt/TokenPrivileges, winnt/TokenRestrictedDeviceClaimAttributes, winnt/TokenRestrictedDeviceGroups, winnt/TokenRestrictedSids, winnt/TokenRestrictedUserClaimAttributes, winnt/TokenSandBoxInert, winnt/TokenSecurityAttributes, winnt/TokenSessionId, winnt/TokenSessionReference, winnt/TokenSource, winnt/TokenStatistics, winnt/TokenType, winnt/TokenUIAccess, winnt/TokenUser, winnt/TokenUserClaimAttributes, winnt/TokenVirtualizationAllowed, winnt/TokenVirtualizationEnabled'
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
req.typenames: TOKEN_INFORMATION_CLASS, *PTOKEN_INFORMATION_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_INFORMATION_CLASS
 - winnt/_TOKEN_INFORMATION_CLASS
 - PTOKEN_INFORMATION_CLASS
 - winnt/PTOKEN_INFORMATION_CLASS
 - TOKEN_INFORMATION_CLASS
 - winnt/TOKEN_INFORMATION_CLASS
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
 - TOKEN_INFORMATION_CLASS
---

# TOKEN_INFORMATION_CLASS enumeration


## -description

The <b>TOKEN_INFORMATION_CLASS</b> enumeration contains values that specify the type of information being assigned to or retrieved from an <a href="/windows/desktop/SecGloss/a-gly">access token</a>.

The <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a> function uses these values to indicate the type of token information to retrieve.

The <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a> function uses these values to set the token information.

## -enum-fields

### -field TokenUser:1

The buffer receives a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a> structure that contains the user account of the token.

### -field TokenGroups

The buffer receives a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that contains the group accounts associated with the token.

### -field TokenPrivileges

The buffer receives a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a> structure that contains the privileges of the token.

### -field TokenOwner

The buffer receives a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_owner">TOKEN_OWNER</a> structure that contains the default owner <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) for newly created objects.

### -field TokenPrimaryGroup

The buffer receives a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_primary_group">TOKEN_PRIMARY_GROUP</a> structure that contains the default primary group SID for newly created objects.

### -field TokenDefaultDacl

The buffer receives a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a> structure that contains the default DACL for newly created objects.

### -field TokenSource

The buffer receives a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a> structure that contains the source of the token. <b>TOKEN_QUERY_SOURCE</b> access is needed to retrieve this information.

### -field TokenType

The buffer receives a 
<a href="/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a> value that indicates whether the token is a <a href="/windows/desktop/SecGloss/p-gly">primary</a> or <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a>.

### -field TokenImpersonationLevel

The buffer receives a 
<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a> value that indicates the impersonation level of the token. If the access token is not an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a>, the function fails.

### -field TokenStatistics

The buffer receives a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_statistics">TOKEN_STATISTICS</a> structure that contains various token statistics.

### -field TokenRestrictedSids

The buffer receives a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that contains the list of restricting SIDs in a 
<a href="/windows/desktop/SecAuthZ/restricted-tokens">restricted token</a>.

### -field TokenSessionId

The buffer receives a <b>DWORD</b> value that indicates the Terminal Services session identifier that is associated with the token.

If the token is associated with the terminal server client session, the session identifier is nonzero.

<b>Windows Server 2003 and Windows XP:  </b>If the token is associated with the terminal server console session, the session identifier is zero.

In a non-Terminal Services environment, the session identifier is zero.

If <b>TokenSessionId</b> is set with <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a>, the application must have the <b>Act As Part Of the Operating System</b> privilege, and the application must be enabled to set the session ID in a token.

### -field TokenGroupsAndPrivileges

The buffer receives a <a href="/windows/desktop/api/winnt/ns-winnt-token_groups_and_privileges">TOKEN_GROUPS_AND_PRIVILEGES</a> structure that contains the user SID, the group accounts, the restricted SIDs, and the authentication ID associated with the token.

### -field TokenSessionReference

Reserved.

### -field TokenSandBoxInert

The buffer receives a <b>DWORD</b> value that is nonzero if the token includes the <b>SANDBOX_INERT</b> flag.

### -field TokenAuditPolicy

Reserved.

### -field TokenOrigin

The buffer receives a <a href="/windows/desktop/api/winnt/ns-winnt-token_origin">TOKEN_ORIGIN</a> value. 

If the token  resulted from a logon that used explicit credentials, such as passing a name, domain, and password to the  <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> function, then the <a href="/windows/desktop/api/winnt/ns-winnt-token_origin">TOKEN_ORIGIN</a> structure will contain the ID of the <a href="/windows/desktop/SecGloss/l-gly">logon session</a> that created it.

If the token resulted from  network authentication, such as a call to <a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext</a>  or a call to <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> with <i>dwLogonType</i> set to <b>LOGON32_LOGON_NETWORK</b> or <b>LOGON32_LOGON_NETWORK_CLEARTEXT</b>, then this value will be zero.

### -field TokenElevationType

The buffer receives a <a href="/windows/desktop/api/winnt/ne-winnt-token_elevation_type">TOKEN_ELEVATION_TYPE</a> value that specifies the elevation level of the token.

### -field TokenLinkedToken

The buffer receives a <a href="/windows/desktop/api/winnt/ns-winnt-token_linked_token">TOKEN_LINKED_TOKEN</a> structure that contains a handle to another token that is linked to this token.

### -field TokenElevation

The buffer receives a <a href="/windows/desktop/api/winnt/ns-winnt-token_elevation">TOKEN_ELEVATION</a> structure that specifies whether the token is elevated.

### -field TokenHasRestrictions

The buffer receives a <b>DWORD</b> value that is nonzero if the token has ever been filtered.

### -field TokenAccessInformation

The buffer receives a <a href="/windows/desktop/api/winnt/ns-winnt-token_access_information">TOKEN_ACCESS_INFORMATION</a> structure that specifies  security information contained in the token.

### -field TokenVirtualizationAllowed

The buffer receives a <b>DWORD</b> value that is nonzero if  <a href="/windows/desktop/SecGloss/v-gly">virtualization</a> is allowed for the token.

### -field TokenVirtualizationEnabled

The buffer receives a <b>DWORD</b> value that is nonzero if  <a href="/windows/desktop/SecGloss/v-gly">virtualization</a> is enabled for the token.

### -field TokenIntegrityLevel

The buffer receives a <a href="/windows/desktop/api/winnt/ns-winnt-token_mandatory_label">TOKEN_MANDATORY_LABEL</a> structure that specifies the token's integrity level.

### -field TokenUIAccess

The buffer receives a <b>DWORD</b> value that is nonzero if  the token has the UIAccess flag set.

### -field TokenMandatoryPolicy

The buffer receives a <a href="/windows/desktop/api/winnt/ns-winnt-token_mandatory_policy">TOKEN_MANDATORY_POLICY</a> structure that specifies the token's mandatory integrity policy.

### -field TokenLogonSid

The buffer receives a <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that specifies the token's logon SID.

### -field TokenIsAppContainer

The buffer receives a <b>DWORD</b> value that is nonzero if the token is an app container token. Any callers who check the <b>TokenIsAppContainer</b> and have it return 0 should also verify that the caller token is not an identify level impersonation token. If the current token is not an app container but is an identity level token, you should return <b>AccessDenied</b>.

### -field TokenCapabilities

The buffer receives a <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that contains the capabilities associated with the token.

### -field TokenAppContainerSid

The buffer receives a <a href="/windows/desktop/api/winnt/ns-winnt-token_appcontainer_information">TOKEN_APPCONTAINER_INFORMATION</a> structure that contains the AppContainerSid associated with the token. If the token is not associated with an app container, the <b>TokenAppContainer</b> member of the <b>TOKEN_APPCONTAINER_INFORMATION</b> structure points to <b>NULL</b>.

### -field TokenAppContainerNumber

The buffer receives a <b>DWORD</b> value that includes the   app container number for the token. For tokens that are not app container tokens, this value is zero.

### -field TokenUserClaimAttributes

The buffer receives a <a href="/windows/desktop/api/winnt/ns-winnt-claim_security_attributes_information">CLAIM_SECURITY_ATTRIBUTES_INFORMATION</a> structure that contains the user claims associated with the token.

### -field TokenDeviceClaimAttributes

The buffer receives  a <a href="/windows/desktop/api/winnt/ns-winnt-claim_security_attributes_information">CLAIM_SECURITY_ATTRIBUTES_INFORMATION</a> structure that contains the  device claims associated with the token.

### -field TokenRestrictedUserClaimAttributes

This value is reserved.

### -field TokenRestrictedDeviceClaimAttributes

This value is reserved.

### -field TokenDeviceGroups

The buffer receives a <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that contains the device groups that are associated with the token.

### -field TokenRestrictedDeviceGroups

The buffer receives a <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that contains the restricted device groups that are associated with the token.

### -field TokenSecurityAttributes

This value is reserved.

### -field TokenIsRestricted

This value is reserved.

### -field TokenProcessTrustLevel

### -field TokenPrivateNameSpace

### -field TokenSingletonAttributes

### -field TokenBnoIsolation

### -field TokenChildProcessFlags

### -field TokenIsLessPrivilegedAppContainer

### -field MaxTokenInfoClass

The maximum value for this enumeration.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-enumerations">Authorization Enumerations</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_control">TOKEN_CONTROL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_device_claims">TOKEN_DEVICE_CLAIMS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups_and_privileges">TOKEN_GROUPS_AND_PRIVILEGES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_origin">TOKEN_ORIGIN</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_owner">TOKEN_OWNER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_primary_group">TOKEN_PRIMARY_GROUP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_statistics">TOKEN_STATISTICS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user_claims">TOKEN_USER_CLAIMS</a>
