---
UID: NS:sspi._SEC_WINNT_AUTH_DATA_TYPE_SMARTCARD_CONTEXTS_DATA
tech.root: security
title: SEC_WINNT_AUTH_DATA_TYPE_SMARTCARD_CONTEXTS_DATA
ms.date: 07/20/2022
targetos: Windows
description: Contains the authentication data for a smartcard context.
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
req.typenames: SEC_WINNT_AUTH_DATA_TYPE_SMARTCARD_CONTEXTS_DATA, *PSEC_WINNT_AUTH_DATA_TYPE_SMARTCARD_CONTEXTS_DATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - _SEC_WINNT_AUTH_DATA_TYPE_SMARTCARD_CONTEXTS_DATA
 - PSEC_WINNT_AUTH_DATA_TYPE_SMARTCARD_CONTEXTS_DATA
 - SEC_WINNT_AUTH_DATA_TYPE_SMARTCARD_CONTEXTS_DATA
f1_keywords:
 - _SEC_WINNT_AUTH_DATA_TYPE_SMARTCARD_CONTEXTS_DATA
 - sspi/_SEC_WINNT_AUTH_DATA_TYPE_SMARTCARD_CONTEXTS_DATA
 - PSEC_WINNT_AUTH_DATA_TYPE_SMARTCARD_CONTEXTS_DATA
 - sspi/PSEC_WINNT_AUTH_DATA_TYPE_SMARTCARD_CONTEXTS_DATA
 - SEC_WINNT_AUTH_DATA_TYPE_SMARTCARD_CONTEXTS_DATA
 - sspi/SEC_WINNT_AUTH_DATA_TYPE_SMARTCARD_CONTEXTS_DATA
dev_langs:
 - c++
helpviewer_keywords:
 - _SEC_WINNT_AUTH_DATA_TYPE_SMARTCARD_CONTEXTS_DATA
---

## -description

Contains the authentication data for a smartcard context.

## -struct-fields

### -field pcc

The smartcard context.

### -field hProv

The handle to the smartcard provider.

### -field pwszECDHKeyName

The name of the Elliptic-curve Diffie–Hellman (ECDH) key. Only optionally set for ECDSA smartcards.

## -remarks

## -see-also
