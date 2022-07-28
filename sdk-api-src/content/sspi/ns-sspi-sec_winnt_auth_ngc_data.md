---
UID: NS:sspi._SEC_WINNT_AUTH_NGC_DATA
tech.root: security
title: SEC_WINNT_AUTH_NGC_DATA
ms.date: 07/20/2022
targetos: Windows
description: Contains the NGC data for authentication.
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
req.typenames: SEC_WINNT_AUTH_NGC_DATA, *PSEC_WINNT_AUTH_NGC_DATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - _SEC_WINNT_AUTH_NGC_DATA
 - PSEC_WINNT_AUTH_NGC_DATA
 - SEC_WINNT_AUTH_NGC_DATA
f1_keywords:
 - _SEC_WINNT_AUTH_NGC_DATA
 - sspi/_SEC_WINNT_AUTH_NGC_DATA
 - PSEC_WINNT_AUTH_NGC_DATA
 - sspi/PSEC_WINNT_AUTH_NGC_DATA
 - SEC_WINNT_AUTH_NGC_DATA
 - sspi/SEC_WINNT_AUTH_NGC_DATA
dev_langs:
 - c++
helpviewer_keywords:
 - _SEC_WINNT_AUTH_NGC_DATA
---

## -description

Contains the NGC data for authentication.

## -struct-fields

### -field LogonId

The logon ID for the user.

### -field Flags

The flags.

### -field CspInfo

The CSP information.

### -field UserIdKeyAuthTicket

The user ID key authentication ticket.

### -field DecryptionKeyName

The name of the decryption key.

### -field DecryptionKeyAuthTicket

The decryption key authentication ticket.

## -remarks

## -see-also
