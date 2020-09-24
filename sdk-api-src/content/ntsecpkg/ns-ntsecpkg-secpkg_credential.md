---
UID: NS:ntsecpkg._SECPKG_CREDENTIAL
title: SECPKG_CREDENTIAL (ntsecpkg.h)
description: Specifies the credentials.
helpviewer_keywords: ["*PSECPKG_CREDENTIAL","PSECPKG_CREDENTIAL","PSECPKG_CREDENTIAL structure pointer [Security]","SECPKG_CREDENTIAL","SECPKG_CREDENTIAL structure [Security]","ntsecpkg/PSECPKG_CREDENTIAL","ntsecpkg/SECPKG_CREDENTIAL","security.secpkg_credential"]
old-location: security\secpkg_credential.htm
tech.root: security
ms.assetid: 67BB382B-E6DB-4E93-90EE-6441751220B9
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_CREDENTIAL, PSECPKG_CREDENTIAL, PSECPKG_CREDENTIAL structure pointer [Security], SECPKG_CREDENTIAL, SECPKG_CREDENTIAL structure [Security], ntsecpkg/PSECPKG_CREDENTIAL, ntsecpkg/SECPKG_CREDENTIAL, security.secpkg_credential'
req.header: ntsecpkg.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SECPKG_CREDENTIAL, *PSECPKG_CREDENTIAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_CREDENTIAL
 - ntsecpkg/_SECPKG_CREDENTIAL
 - PSECPKG_CREDENTIAL
 - ntsecpkg/PSECPKG_CREDENTIAL
 - SECPKG_CREDENTIAL
 - ntsecpkg/SECPKG_CREDENTIAL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_CREDENTIAL
---

# SECPKG_CREDENTIAL structure


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

The supplied credentials that are marshaled. This member contains a <a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential">SECPKG_SUPPLIED_CREDENTIAL</a> 	structure.