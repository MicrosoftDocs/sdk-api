---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _AUTHZ_CONTEXT_INFORMATION_CLASS enumeration


## -description


The <b>AUTHZ_CONTEXT_INFORMATION_CLASS</b> enumeration specifies the type of information to be retrieved from an existing AuthzClientContext. This enumeration is used by the  <a href="https://msdn.microsoft.com/c365029a-3ff3-49c1-9dfc-b52948e466f3">AuthzGetInformationFromContext</a> function.


## -enum-fields




### -field AuthzContextInfoUserSid

Retrieves a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556855">TOKEN_USER</a> structure that contains a user <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) and its attribute.


### -field AuthzContextInfoGroupsSids

Retrieves a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a> structure that contains the group SIDs to which the user belongs and their attributes.


### -field AuthzContextInfoRestrictedSids

Retrieves a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a> structure that contains the restricted group SIDs in the context and their attributes.


### -field AuthzContextInfoPrivileges

Retrieves a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556846">TOKEN_PRIVILEGES</a> structure that contains the privileges held by the user.


### -field AuthzContextInfoExpirationTime

Retrieves the expiration time set on the context.


### -field AuthzContextInfoServerContext

This constant is reserved. Do not use it.


### -field AuthzContextInfoIdentifier

Retrieves an <a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> structures used by the resource manager to identify the context.


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

Retrieves a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a> structure that contains device SIDs and their attributes.

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

Retrieves a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a> structure that contains capability SIDs.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.


## -see-also




<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/c365029a-3ff3-49c1-9dfc-b52948e466f3">AuthzGetInformationFromContext</a>



<a href="https://msdn.microsoft.com/1A865519-E042-4871-886C-9AA64D71CCE4">SECURITY_CAPABILITIES</a>



<a href="https://msdn.microsoft.com/6038C7E9-AED6-49D2-8D96-907E973A64B1">TOKEN_APPCONTAINER_INFORMATION</a>



<a href="https://msdn.microsoft.com/FF20B64C-BD5F-45F5-83F1-B52634BE1065">TOKEN_DEVICE_CLAIMS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556846">TOKEN_PRIVILEGES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556855">TOKEN_USER</a>



<a href="https://msdn.microsoft.com/730541ED-0E33-4F19-BB99-145131161355">TOKEN_USER_CLAIMS</a>
 

 

