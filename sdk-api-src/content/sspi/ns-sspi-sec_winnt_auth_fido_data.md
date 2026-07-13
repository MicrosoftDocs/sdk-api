---
UID: NS:sspi._SEC_WINNT_AUTH_FIDO_DATA
tech.root: security
title: SEC_WINNT_AUTH_FIDO_DATA
ms.date: 07/20/2022
targetos: Windows
description: Contains data for FIDO authentication.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: sspi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: SEC_WINNT_AUTH_FIDO_DATA, *PSEC_WINNT_AUTH_FIDO_DATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - _SEC_WINNT_AUTH_FIDO_DATA
 - PSEC_WINNT_AUTH_FIDO_DATA
 - SEC_WINNT_AUTH_FIDO_DATA
f1_keywords:
 - _SEC_WINNT_AUTH_FIDO_DATA
 - sspi/_SEC_WINNT_AUTH_FIDO_DATA
 - PSEC_WINNT_AUTH_FIDO_DATA
 - sspi/PSEC_WINNT_AUTH_FIDO_DATA
 - SEC_WINNT_AUTH_FIDO_DATA
 - sspi/SEC_WINNT_AUTH_FIDO_DATA
dev_langs:
 - c++
helpviewer_keywords:
 - _SEC_WINNT_AUTH_FIDO_DATA
---

## -description

Contains data for FIDO authentication.

## -struct-fields

### -field cbHeaderLength

The header length, in bytes.

### -field cbStructureLength

The length of the structure, in bytes.

### -field Secret

The secret. Offsets are from the beginning of this structure.

### -field NewSecret

The new secret.

### -field EncryptedNewSecret

The new secret, encrypted. For storage by cloud AP.

### -field NetworkLogonBuffer

Opaque data, which is understood by plugin. May contain signed Nonce and other data to perform a network logon.

### -field ulSignatureCount

The signature count to be stored in public cached information, required for CredProv.

## -remarks

## -see-also
