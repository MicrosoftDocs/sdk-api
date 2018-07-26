---
UID: NE:winnt._SECURITY_IMPERSONATION_LEVEL
title: "_SECURITY_IMPERSONATION_LEVEL"
author: windows-sdk-content
description: Contains values that specify security impersonation levels. Security impersonation levels govern the degree to which a server process can act on behalf of a client process.
old-location: security\security_impersonation_level.htm
old-project: secauthz
ms.assetid: a75ad777-c88e-4899-be50-0118c113a600
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: "*PSECURITY_IMPERSONATION_LEVEL, PSECURITY_IMPERSONATION_LEVEL, PSECURITY_IMPERSONATION_LEVEL enumeration pointer [Security], SECURITY_IMPERSONATION_LEVEL, SECURITY_IMPERSONATION_LEVEL enumeration [Security], SecurityAnonymous, SecurityDelegation, SecurityIdentification, SecurityImpersonation, _SECURITY_IMPERSONATION_LEVEL, _win32_security_impersonation_level_str, security.security_impersonation_level, winnt/PSECURITY_IMPERSONATION_LEVEL, winnt/SECURITY_IMPERSONATION_LEVEL, winnt/SecurityAnonymous, winnt/SecurityDelegation, winnt/SecurityIdentification, winnt/SecurityImpersonation"
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
tech.root: 
req.typenames: SECURITY_IMPERSONATION_LEVEL, *PSECURITY_IMPERSONATION_LEVEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - SECURITY_IMPERSONATION_LEVEL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _SECURITY_IMPERSONATION_LEVEL enumeration


## -description



			The <b>SECURITY_IMPERSONATION_LEVEL</b> enumeration contains values that specify security impersonation levels. Security impersonation levels govern the degree to which a server process can act on behalf of a client <a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">process</a>.


## -enum-fields




### -field SecurityAnonymous

The server process cannot obtain identification information about the client, and it cannot impersonate the client. It is defined with no value given, and thus, by ANSI C rules, defaults to a value of zero.


### -field SecurityIdentification

The server process can obtain information about the client, such as security identifiers and <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">privileges</a>, but it cannot impersonate the client. This is useful for servers that export their own objects, for example, database products that export tables and views. Using the retrieved client-security information, the server can make access-validation decisions without being able to use other services that are using the client's <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>.


### -field SecurityImpersonation

The server process can impersonate the client's security context on its local system. The server cannot impersonate the client on remote systems.


### -field SecurityDelegation

The server process can impersonate the client's security context on remote systems. 





## -remarks



Impersonation is the ability of a process to take on the security attributes of another process.




## -see-also




<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/5f4832b6-5cf5-4050-9e20-56674f2e2cb1">CreatePrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/796ec60e-fcae-48a9-b471-de3dce831306">DuplicateToken</a>



<a href="https://msdn.microsoft.com/96b13826-0ac7-4d70-9c21-eeb343f6b823">DuplicateTokenEx</a>



<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>



<a href="https://msdn.microsoft.com/f909e3a7-6c7f-4c05-aa2e-e637113804c9">ImpersonateSelf</a>



<a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a>
 

 

