---
UID: NE:authz._AUTHZ_CONTEXT_INFORMATION_CLASS
title: AUTHZ_CONTEXT_INFORMATION_CLASS (authz.h)
author: windows-sdk-content
description: Specifies the type of information to be retrieved from an existing AuthzClientContext. This enumeration is used by the AuthzGetInformationFromContext function.
old-location: security\authz_context_information_class.htm
tech.root: SecAuthZ
ms.assetid: 5eb752dc-17f7-4510-8aef-d18280322e76
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AUTHZ_CONTEXT_INFORMATION_CLASS, AUTHZ_CONTEXT_INFORMATION_CLASS enumeration [Security], AuthzContextInfoAll, AuthzContextInfoAppContainerSid, AuthzContextInfoAuthenticationId, AuthzContextInfoCapabilitySids, AuthzContextInfoDeviceClaims, AuthzContextInfoDeviceSids, AuthzContextInfoExpirationTime, AuthzContextInfoGroupsSids, AuthzContextInfoIdentifier, AuthzContextInfoPrivileges, AuthzContextInfoRestrictedSids, AuthzContextInfoSecurityAttributes, AuthzContextInfoServerContext, AuthzContextInfoSource, AuthzContextInfoUserClaims, AuthzContextInfoUserSid, _win32_authz_context_information_class_str, authz/AUTHZ_CONTEXT_INFORMATION_CLASS, authz/AuthzContextInfoAll, authz/AuthzContextInfoAppContainerSid, authz/AuthzContextInfoAuthenticationId, authz/AuthzContextInfoCapabilitySids, authz/AuthzContextInfoDeviceClaims, authz/AuthzContextInfoDeviceSids, authz/AuthzContextInfoExpirationTime, authz/AuthzContextInfoGroupsSids, authz/AuthzContextInfoIdentifier, authz/AuthzContextInfoPrivileges, authz/AuthzContextInfoRestrictedSids, authz/AuthzContextInfoSecurityAttributes, authz/AuthzContextInfoServerContext, authz/AuthzContextInfoSource, authz/AuthzContextInfoUserClaims, authz/AuthzContextInfoUserSid, security.authz_context_information_class
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Authz.h
api_name:
 - AUTHZ_CONTEXT_INFORMATION_CLASS
product: Windows
targetos: Windows
req.typenames: AUTHZ_CONTEXT_INFORMATION_CLASS
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# AUTHZ_CONTEXT_INFORMATION_CLASS enumeration


## -description


The <b>AUTHZ_CONTEXT_INFORMATION_CLASS</b> enumeration specifies the type of information to be retrieved from an existing AuthzClientContext. This enumeration is used by the  <a href="https://msdn.microsoft.com/c365029a-3ff3-49c1-9dfc-b52948e466f3">AuthzGetInformationFromContext</a> function.


## -enum-fields




### -field AuthzContextInfoUserSid

Retrieves a <a href="https://msdn.microsoft.com/5dd8172d-7b1a-4cc0-b667-5fe91d278393">TOKEN_USER</a> structure that contains a user <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) and its attribute.


### -field AuthzContextInfoGroupsSids

Retrieves a <a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure that contains the group SIDs to which the user belongs and their attributes.


### -field AuthzContextInfoRestrictedSids

Retrieves a <a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure that contains the restricted group SIDs in the context and their attributes.


### -field AuthzContextInfoPrivileges

Retrieves a <a href="https://msdn.microsoft.com/c9016511-740f-44f3-92ed-17cc518c6612">TOKEN_PRIVILEGES</a> structure that contains the privileges held by the user.


### -field AuthzContextInfoExpirationTime

Retrieves the expiration time set on the context.


### -field AuthzContextInfoServerContext

This constant is reserved. Do not use it.


### -field AuthzContextInfoIdentifier

Retrieves an <a href="https://msdn.microsoft.com/a812a46b-f23f-45b1-a6c6-48f931b78750">LUID</a> structures used by the resource manager to identify the context.


### -field AuthzContextInfoSource

This constant is reserved. Do not use it.


### -field AuthzContextInfoAll

This constant is reserved. Do not use it.


### -field AuthzContextInfoAuthenticationId

This constant is reserved. Do not use it.


### -field AuthzContextInfoSecurityAttributes

Retrieves an <a href="https://msdn.microsoft.com/1db95ab0-951f-488c-b522-b3f38fc74c7c">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure that contains security attributes.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.


### -field AuthzContextInfoDeviceSids

Retrieves a <a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure that contains device SIDs and their attributes.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.


### -field AuthzContextInfoUserClaims

Retrieves a <a href="https://msdn.microsoft.com/1db95ab0-951f-488c-b522-b3f38fc74c7c">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure that contains user claims.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.


### -field AuthzContextInfoDeviceClaims

Retrieves a <a href="https://msdn.microsoft.com/1db95ab0-951f-488c-b522-b3f38fc74c7c">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure that contains device claims.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.


### -field AuthzContextInfoAppContainerSid

Retrieves a <a href="https://msdn.microsoft.com/6038C7E9-AED6-49D2-8D96-907E973A64B1">TOKEN_APPCONTAINER_INFORMATION</a> structure that contains the app container SID.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.


### -field AuthzContextInfoCapabilitySids

Retrieves a <a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure that contains capability SIDs.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.


## -see-also




<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/c365029a-3ff3-49c1-9dfc-b52948e466f3">AuthzGetInformationFromContext</a>



<a href="https://msdn.microsoft.com/1A865519-E042-4871-886C-9AA64D71CCE4">SECURITY_CAPABILITIES</a>



<a href="https://msdn.microsoft.com/6038C7E9-AED6-49D2-8D96-907E973A64B1">TOKEN_APPCONTAINER_INFORMATION</a>



<a href="https://msdn.microsoft.com/FF20B64C-BD5F-45F5-83F1-B52634BE1065">TOKEN_DEVICE_CLAIMS</a>



<a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a>



<a href="https://msdn.microsoft.com/c9016511-740f-44f3-92ed-17cc518c6612">TOKEN_PRIVILEGES</a>



<a href="https://msdn.microsoft.com/5dd8172d-7b1a-4cc0-b667-5fe91d278393">TOKEN_USER</a>



<a href="https://msdn.microsoft.com/730541ED-0E33-4F19-BB99-145131161355">TOKEN_USER_CLAIMS</a>
 

 

