---
UID: NS:ntsecpkg._SECPKG_CLIENT_INFO
title: "_SECPKG_CLIENT_INFO"
author: windows-sdk-content
description: The SECPKG_CLIENT_INFO structure holds information about a security package's client. This structure is used by the GetClientInfo function.
old-location: security\secpkg_client_info.htm
tech.root: secauthn
ms.assetid: c9c58a50-7fc2-44a7-9551-a2675410b2b5
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*PSECPKG_CLIENT_INFO, PSECPKG_CLIENT_INFO, PSECPKG_CLIENT_INFO structure pointer [Security], SECPKG_CLIENT_INFO, SECPKG_CLIENT_INFO structure [Security], _SECPKG_CLIENT_INFO, _ssp_secpkg_client_info, ntsecpkg/PSECPKG_CLIENT_INFO, ntsecpkg/SECPKG_CLIENT_INFO, security.secpkg_client_info"
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
 - SECPKG_CLIENT_INFO
product: Windows
targetos: Windows
req.typenames: SECPKG_CLIENT_INFO, *PSECPKG_CLIENT_INFO
req.redist: 
---

# _SECPKG_CLIENT_INFO structure


## -description


The <b>SECPKG_CLIENT_INFO</b> structure holds information about a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package's</a> client. This structure is used by the 
<a href="https://msdn.microsoft.com/3669f2e2-da70-4195-bdd0-f8415d97ae99">GetClientInfo</a> function.


## -struct-fields




### -field LogonId

The client's effective <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon identifier</a>.


### -field ProcessID

The client's process identifier.


### -field ThreadID

The client's thread identifier.


### -field HasTcbPrivilege

<b>TRUE</b> if the client has the SeTcbPrivilege privilege; otherwise <b>FALSE</b>.


### -field Impersonating

<b>TRUE</b> if the client is impersonating another <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security principal</a>.


### -field Restricted

The client is restricted in its ability to access securable objects or perform privileged operations.


### -field ClientFlags

 


### -field ImpersonationLevel

 


### -field ClientToken

 



