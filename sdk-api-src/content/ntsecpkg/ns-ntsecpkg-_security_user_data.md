---
UID: NS:ntsecpkg._SECURITY_USER_DATA
title: "_SECURITY_USER_DATA"
author: windows-sdk-content
description: The SecurityUserData structure contains information about the user of a security support provider/authentication package. This structure is used by the SpGetUserInfo function.
old-location: security\securityuserdata.htm
tech.root: SecAuthN
ms.assetid: 1a56203a-ed6a-4f32-9e7c-b498ba61a64b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PSECURITY_USER_DATA, *PSecurityUserData, PSECURITY_USER_DATA, PSECURITY_USER_DATA structure pointer [Security], PSecurityUserData, PSecurityUserData structure pointer [Security], SECURITY_USER_DATA, SECURITY_USER_DATA structure [Security], SecurityUserData, SecurityUserData structure [Security], _SECURITY_USER_DATA, _ssp_securityuserdata, ntsecpkg/PSECURITY_USER_DATA, ntsecpkg/PSecurityUserData, ntsecpkg/SecurityUserData, security.securityuserdata"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECURITY_USER_DATA
product: Windows
targetos: Windows
req.typenames: SECURITY_USER_DATA, *PSECURITY_USER_DATA
req.redist: 
---

# _SECURITY_USER_DATA structure


## -description


The <b>SecurityUserData</b> structure contains information about the user of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a>/<a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authentication package</a>. This structure is used by the 
<a href="https://msdn.microsoft.com/ee37fab0-5ee5-4cc5-9fcc-5c74cb0b2b26">SpGetUserInfo</a> function.


## -struct-fields




### -field UserName

The name of the user.


### -field LogonDomainName

The domain the user is logged onto.


### -field LogonServer

The name of the server that logged the user on.


### -field pSid

The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) of the user.

