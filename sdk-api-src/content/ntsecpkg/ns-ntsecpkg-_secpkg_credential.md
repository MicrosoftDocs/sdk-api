---
UID: NS:ntsecpkg._SECPKG_CREDENTIAL
title: "_SECPKG_CREDENTIAL"
author: windows-sdk-content
description: Specifies the credentials.
old-location: security\secpkg_credential.htm
old-project: secauthn
ms.assetid: 67BB382B-E6DB-4E93-90EE-6441751220B9
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: "*PSECPKG_CREDENTIAL, PSECPKG_CREDENTIAL, PSECPKG_CREDENTIAL structure pointer [Security], SECPKG_CREDENTIAL, SECPKG_CREDENTIAL structure [Security], _SECPKG_CREDENTIAL, ntsecpkg/PSECPKG_CREDENTIAL, ntsecpkg/SECPKG_CREDENTIAL, security.secpkg_credential"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecpkg.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: SECPKG_CREDENTIAL, *PSECPKG_CREDENTIAL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_CREDENTIAL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _SECPKG_CREDENTIAL structure


## -description


Specifies the credentials.


## -struct-fields




### -field Version

The version. 


### -field cbHeaderLength

The length of the header.


### -field cbStructureLength

The length of the structure, including the header, so that all of the content is in a contiguous buffer.


### -field ClientProcess

The identity of the client process.


### -field ClientThread

The identity of the client thread.


### -field LogonId

The logon identity of the caller.


### -field ClientToken

The client token of the caller.


### -field SessionId

The session identity of the caller.


### -field ModifiedId

The modified identity of the caller.


### -field fCredentials

The credentials that are passed in or returned.


### -field Flags

The credential flags.


### -field PrincipalName

Not currently used.


### -field PackageList

The list of packages. This member is only relevant to SPNego.


### -field MarshaledSuppliedCreds

The supplied credentials that are marshaled. This member contains a <a href="https://msdn.microsoft.com/23849312-7AC5-4D09-8889-27DFF8E32FE8">SECPKG_SUPPLIED_CREDENTIAL</a> 	structure.

