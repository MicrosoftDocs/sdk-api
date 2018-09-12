---
UID: NE:winnt._TOKEN_INFORMATION_CLASS
title: "_TOKEN_INFORMATION_CLASS"
author: windows-sdk-content
description: Contains values that specify the type of information being assigned to or retrieved from an access token.
old-location: security\token_information_class.htm
tech.root: SecAuthZ
ms.assetid: cb606665-1266-4e71-a145-9b04bf157cdc
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PTOKEN_INFORMATION_CLASS, MaxTokenInfoClass, PTOKEN_INFORMATION_CLASS, PTOKEN_INFORMATION_CLASS enumeration pointer [Security], TOKEN_INFORMATION_CLASS, TOKEN_INFORMATION_CLASS enumeration [Security], TokenAccessInformation, TokenAppContainerNumber, TokenAppContainerSid, TokenAuditPolicy, TokenCapabilities, TokenDefaultDacl, TokenDeviceClaimAttributes, TokenDeviceGroups, TokenElevation, TokenElevationType, TokenGroups, TokenGroupsAndPrivileges, TokenHasRestrictions, TokenImpersonationLevel, TokenIntegrityLevel, TokenIsAppContainer, TokenIsRestricted, TokenLinkedToken, TokenLogonSid, TokenMandatoryPolicy, TokenOrigin, TokenOwner, TokenPrimaryGroup, TokenPrivileges, TokenRestrictedDeviceClaimAttributes, TokenRestrictedDeviceGroups, TokenRestrictedSids, TokenRestrictedUserClaimAttributes, TokenSandBoxInert, TokenSecurityAttributes, TokenSessionId, TokenSessionReference, TokenSource, TokenStatistics, TokenType, TokenUIAccess, TokenUser, TokenUserClaimAttributes, TokenVirtualizationAllowed, TokenVirtualizationEnabled, _TOKEN_INFORMATION_CLASS, _win32_token_information_class_str, security.token_information_class, winnt/MaxTokenInfoClass, winnt/PTOKEN_INFORMATION_CLASS, winnt/TOKEN_INFORMATION_CLASS, winnt/TokenAccessInformation, winnt/TokenAppContainerNumber, winnt/TokenAppContainerSid, winnt/TokenAuditPolicy, winnt/TokenCapabilities, winnt/TokenDefaultDacl, winnt/TokenDeviceClaimAttributes, winnt/TokenDeviceGroups, winnt/TokenElevation, winnt/TokenElevationType, winnt/TokenGroups, winnt/TokenGroupsAndPrivileges, winnt/TokenHasRestrictions, winnt/TokenImpersonationLevel, winnt/TokenIntegrityLevel, winnt/TokenIsAppContainer, winnt/TokenIsRestricted, winnt/TokenLinkedToken, winnt/TokenLogonSid, winnt/TokenMandatoryPolicy, winnt/TokenOrigin, winnt/TokenOwner, winnt/TokenPrimaryGroup, winnt/TokenPrivileges, winnt/TokenRestrictedDeviceClaimAttributes, winnt/TokenRestrictedDeviceGroups, winnt/TokenRestrictedSids, winnt/TokenRestrictedUserClaimAttributes, winnt/TokenSandBoxInert, winnt/TokenSecurityAttributes, winnt/TokenSessionId, winnt/TokenSessionReference, winnt/TokenSource, winnt/TokenStatistics, winnt/TokenType, winnt/TokenUIAccess, winnt/TokenUser, winnt/TokenUserClaimAttributes, winnt/TokenVirtualizationAllowed, winnt/TokenVirtualizationEnabled"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_INFORMATION_CLASS
product: Windows
targetos: Windows
req.typenames: TOKEN_INFORMATION_CLASS, *PTOKEN_INFORMATION_CLASS
req.redist: 
---

# _TOKEN_INFORMATION_CLASS enumeration


## -description


The <b>TOKEN_INFORMATION_CLASS</b> enumeration contains values that specify the type of information being assigned to or retrieved from an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a>.

The <a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a> function uses these values to indicate the type of token information to retrieve.

The <a href="https://msdn.microsoft.com/cdb8af74-540d-4059-ac64-6243f6aabaa6">SetTokenInformation</a> function uses these values to set the token information.


## -enum-fields




### -field TokenUser

The buffer receives a 
<a href="https://msdn.microsoft.com/5dd8172d-7b1a-4cc0-b667-5fe91d278393">TOKEN_USER</a> structure that contains the user account of the token.


### -field TokenGroups

The buffer receives a 
<a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure that contains the group accounts associated with the token.


### -field TokenPrivileges

The buffer receives a 
<a href="https://msdn.microsoft.com/c9016511-740f-44f3-92ed-17cc518c6612">TOKEN_PRIVILEGES</a> structure that contains the privileges of the token.


### -field TokenOwner

The buffer receives a 
<a href="https://msdn.microsoft.com/85617d56-ad46-40a3-a335-121f3c8edcc3">TOKEN_OWNER</a> structure that contains the default owner <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) for newly created objects.


### -field TokenPrimaryGroup

The buffer receives a 
<a href="https://msdn.microsoft.com/d23ebe6c-36a3-434a-a0fa-fcdf50dd19a0">TOKEN_PRIMARY_GROUP</a> structure that contains the default primary group SID for newly created objects.


### -field TokenDefaultDacl

The buffer receives a 
<a href="https://msdn.microsoft.com/29fb738f-1ecd-4b72-9aea-64698cd74c12">TOKEN_DEFAULT_DACL</a> structure that contains the default DACL for newly created objects.


### -field TokenSource

The buffer receives a 
<a href="https://msdn.microsoft.com/9c533327-e4a0-4852-828c-622d190b7d1e">TOKEN_SOURCE</a> structure that contains the source of the token. <b>TOKEN_QUERY_SOURCE</b> access is needed to retrieve this information.


### -field TokenType

The buffer receives a 
<a href="https://msdn.microsoft.com/51b6717e-3fda-4af4-8995-4ac571eae2fd">TOKEN_TYPE</a> value that indicates whether the token is a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary</a> or <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>.


### -field TokenImpersonationLevel

The buffer receives a 
<a href="https://msdn.microsoft.com/a75ad777-c88e-4899-be50-0118c113a600">SECURITY_IMPERSONATION_LEVEL</a> value that indicates the impersonation level of the token. If the access token is not an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>, the function fails.


### -field TokenStatistics

The buffer receives a 
<a href="https://msdn.microsoft.com/7fcc4a46-1bac-49c1-a239-b466d3bf31d9">TOKEN_STATISTICS</a> structure that contains various token statistics.


### -field TokenRestrictedSids

The buffer receives a 
<a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure that contains the list of restricting SIDs in a 
<a href="https://msdn.microsoft.com/06580ab9-ff58-4aa9-bf88-9536a2e1981d">restricted token</a>.


### -field TokenSessionId

The buffer receives a <b>DWORD</b> value that indicates the Terminal Services session identifier that is associated with the token.

If the token is associated with the terminal server client session, the session identifier is nonzero.

<b>Windows Server 2003 and Windows XP:  </b>If the token is associated with the terminal server console session, the session identifier is zero.

In a non-Terminal Services environment, the session identifier is zero.

If <b>TokenSessionId</b> is set with <a href="https://msdn.microsoft.com/cdb8af74-540d-4059-ac64-6243f6aabaa6">SetTokenInformation</a>, the application must have the <b>Act As Part Of the Operating System</b> privilege, and the application must be enabled to set the session ID in a token.


### -field TokenGroupsAndPrivileges

The buffer receives a <a href="https://msdn.microsoft.com/085ccd0a-d6c2-48ca-ad2a-933f22831b14">TOKEN_GROUPS_AND_PRIVILEGES</a> structure that contains the user SID, the group accounts, the restricted SIDs, and the authentication ID associated with the token.


### -field TokenSessionReference

Reserved.


### -field TokenSandBoxInert

The buffer receives a <b>DWORD</b> value that is nonzero if the token includes the <b>SANDBOX_INERT</b> flag.


### -field TokenAuditPolicy

Reserved.


### -field TokenOrigin

The buffer receives a <a href="https://msdn.microsoft.com/b613f76a-7ad1-4066-90a1-244974f10219">TOKEN_ORIGIN</a> value. 

If the token  resulted from a logon that used explicit credentials, such as passing a name, domain, and password to the  <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> function, then the <a href="https://msdn.microsoft.com/b613f76a-7ad1-4066-90a1-244974f10219">TOKEN_ORIGIN</a> structure will contain the ID of the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a> that created it.

If the token resulted from  network authentication, such as a call to <a href="security.acceptsecuritycontext">AcceptSecurityContext</a>  or a call to <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> with <i>dwLogonType</i> set to <b>LOGON32_LOGON_NETWORK</b> or <b>LOGON32_LOGON_NETWORK_CLEARTEXT</b>, then this value will be zero.


### -field TokenElevationType

The buffer receives a <a href="https://msdn.microsoft.com/bfdfa7b3-a8a9-4e54-896c-4be97521a079">TOKEN_ELEVATION_TYPE</a> value that specifies the elevation level of the token.


### -field TokenLinkedToken

The buffer receives a <a href="https://msdn.microsoft.com/a77dd410-1074-4196-8323-ccf52ed0375a">TOKEN_LINKED_TOKEN</a> structure that contains a handle to another token that is linked to this token.


### -field TokenElevation

The buffer receives a <a href="https://msdn.microsoft.com/a1c87818-f092-43cf-872d-4bb2590a944b">TOKEN_ELEVATION</a> structure that specifies whether the token is elevated.


### -field TokenHasRestrictions

The buffer receives a <b>DWORD</b> value that is nonzero if the token has ever been filtered.


### -field TokenAccessInformation

The buffer receives a <a href="https://msdn.microsoft.com/cb727b91-c88f-48f3-8329-020d3f727dc7">TOKEN_ACCESS_INFORMATION</a> structure that specifies  security information contained in the token.


### -field TokenVirtualizationAllowed

The buffer receives a <b>DWORD</b> value that is nonzero if  <a href="https://msdn.microsoft.com/412796ce-2ad5-429b-a2a6-8d286b19ae30">virtualization</a> is allowed for the token.


### -field TokenVirtualizationEnabled

The buffer receives a <b>DWORD</b> value that is nonzero if  <a href="https://msdn.microsoft.com/412796ce-2ad5-429b-a2a6-8d286b19ae30">virtualization</a> is enabled for the token.


### -field TokenIntegrityLevel

The buffer receives a <a href="https://msdn.microsoft.com/cf37eb34-ee90-43c6-97a9-c5edfcba2bc5">TOKEN_MANDATORY_LABEL</a> structure that specifies the token's integrity level. 


### -field TokenUIAccess

The buffer receives a <b>DWORD</b> value that is nonzero if  the token has the UIAccess flag set.


### -field TokenMandatoryPolicy

The buffer receives a <a href="https://msdn.microsoft.com/f5fc438b-c4f0-46f6-a188-52ce660d13da">TOKEN_MANDATORY_POLICY</a> structure that specifies the token's mandatory integrity policy.


### -field TokenLogonSid

The buffer receives a <a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure that specifies the token's logon SID.


### -field TokenIsAppContainer

The buffer receives a <b>DWORD</b> value that is nonzero if the token is an app container token. Any callers who check the <b>TokenIsAppContainer</b> and have it return 0 should also verify that the caller token is not an identify level impersonation token. If the current token is not an app container but is an identity level token, you should return <b>AccessDenied</b>.


### -field TokenCapabilities

The buffer receives a <a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure that contains the capabilities associated with the token.


### -field TokenAppContainerSid

The buffer receives a <a href="https://msdn.microsoft.com/6038C7E9-AED6-49D2-8D96-907E973A64B1">TOKEN_APPCONTAINER_INFORMATION</a> structure that contains the AppContainerSid associated with the token. If the token is not associated with an app container, the <b>TokenAppContainer</b> member of the <b>TOKEN_APPCONTAINER_INFORMATION</b> structure points to <b>NULL</b>.


### -field TokenAppContainerNumber

The buffer receives a <b>DWORD</b> value that includes the   app container number for the token. For tokens that are not app container tokens, this value is zero.


### -field TokenUserClaimAttributes

The buffer receives a <a href="https://msdn.microsoft.com/D7D9816E-1ECE-48CA-9F2F-0955572A0FCA">CLAIM_SECURITY_ATTRIBUTES_INFORMATION</a> structure that contains the user claims associated with the token.


### -field TokenDeviceClaimAttributes

The buffer receives  a <a href="https://msdn.microsoft.com/D7D9816E-1ECE-48CA-9F2F-0955572A0FCA">CLAIM_SECURITY_ATTRIBUTES_INFORMATION</a> structure that contains the  device claims associated with the token.


### -field TokenRestrictedUserClaimAttributes

This value is reserved.


### -field TokenRestrictedDeviceClaimAttributes

This value is reserved.


### -field TokenDeviceGroups

The buffer receives a <a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure that contains the device groups that are associated with the token.


### -field TokenRestrictedDeviceGroups

The buffer receives a <a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure that contains the restricted device groups that are associated with the token.


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




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>



<a href="https://msdn.microsoft.com/a75ad777-c88e-4899-be50-0118c113a600">SECURITY_IMPERSONATION_LEVEL</a>



<a href="https://msdn.microsoft.com/cdb8af74-540d-4059-ac64-6243f6aabaa6">SetTokenInformation</a>



<a href="https://msdn.microsoft.com/b87c942b-8e58-471d-8cdf-e46cdac647c4">TOKEN_CONTROL</a>



<a href="https://msdn.microsoft.com/29fb738f-1ecd-4b72-9aea-64698cd74c12">TOKEN_DEFAULT_DACL</a>



<a href="https://msdn.microsoft.com/FF20B64C-BD5F-45F5-83F1-B52634BE1065">TOKEN_DEVICE_CLAIMS</a>



<a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a>



<a href="https://msdn.microsoft.com/085ccd0a-d6c2-48ca-ad2a-933f22831b14">TOKEN_GROUPS_AND_PRIVILEGES</a>



<a href="https://msdn.microsoft.com/b613f76a-7ad1-4066-90a1-244974f10219">TOKEN_ORIGIN</a>



<a href="https://msdn.microsoft.com/85617d56-ad46-40a3-a335-121f3c8edcc3">TOKEN_OWNER</a>



<a href="https://msdn.microsoft.com/d23ebe6c-36a3-434a-a0fa-fcdf50dd19a0">TOKEN_PRIMARY_GROUP</a>



<a href="https://msdn.microsoft.com/c9016511-740f-44f3-92ed-17cc518c6612">TOKEN_PRIVILEGES</a>



<a href="https://msdn.microsoft.com/9c533327-e4a0-4852-828c-622d190b7d1e">TOKEN_SOURCE</a>



<a href="https://msdn.microsoft.com/7fcc4a46-1bac-49c1-a239-b466d3bf31d9">TOKEN_STATISTICS</a>



<a href="https://msdn.microsoft.com/51b6717e-3fda-4af4-8995-4ac571eae2fd">TOKEN_TYPE</a>



<a href="https://msdn.microsoft.com/5dd8172d-7b1a-4cc0-b667-5fe91d278393">TOKEN_USER</a>



<a href="https://msdn.microsoft.com/730541ED-0E33-4F19-BB99-145131161355">TOKEN_USER_CLAIMS</a>
 

 

