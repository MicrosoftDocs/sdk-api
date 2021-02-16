---
UID: NS:sspi._SEC_WINNT_AUTH_SHORT_VECTOR
title: SEC_WINNT_AUTH_SHORT_VECTOR (sspi.h)
description: Specifies the offset and number of characters in an array of USHORT values.
helpviewer_keywords: ["*PSEC_WINNT_AUTH_SHORT_VECTOR","PSEC_WINNT_AUTH_SHORT_VECTOR","PSEC_WINNT_AUTH_SHORT_VECTOR structure pointer [Security]","SEC_WINNT_AUTH_SHORT_VECTOR","SEC_WINNT_AUTH_SHORT_VECTOR structure [Security]","security.sec_winnt_auth_short_vector","sspi/PSEC_WINNT_AUTH_SHORT_VECTOR","sspi/SEC_WINNT_AUTH_SHORT_VECTOR"]
old-location: security\sec_winnt_auth_short_vector.htm
tech.root: security
ms.assetid: c3c1ade7-db2b-4450-97c1-5b67e4ebdcb0
ms.date: 12/05/2018
ms.keywords: '*PSEC_WINNT_AUTH_SHORT_VECTOR, PSEC_WINNT_AUTH_SHORT_VECTOR, PSEC_WINNT_AUTH_SHORT_VECTOR structure pointer [Security], SEC_WINNT_AUTH_SHORT_VECTOR, SEC_WINNT_AUTH_SHORT_VECTOR structure [Security], security.sec_winnt_auth_short_vector, sspi/PSEC_WINNT_AUTH_SHORT_VECTOR, sspi/SEC_WINNT_AUTH_SHORT_VECTOR'
req.header: sspi.h
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
req.typenames: SEC_WINNT_AUTH_SHORT_VECTOR, *PSEC_WINNT_AUTH_SHORT_VECTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SEC_WINNT_AUTH_SHORT_VECTOR
 - sspi/_SEC_WINNT_AUTH_SHORT_VECTOR
 - PSEC_WINNT_AUTH_SHORT_VECTOR
 - sspi/PSEC_WINNT_AUTH_SHORT_VECTOR
 - SEC_WINNT_AUTH_SHORT_VECTOR
 - sspi/SEC_WINNT_AUTH_SHORT_VECTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SEC_WINNT_AUTH_SHORT_VECTOR
---

# SEC_WINNT_AUTH_SHORT_VECTOR structure


## -description

Specifies the offset and number of characters in an array of <b>USHORT</b> values.

## -struct-fields

### -field ShortArrayOffset

The number of characters before the beginning of the data in a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_packed_credentials_ex">SEC_WINNT_AUTH_PACKED_CREDENTIALS_EX</a> structure.

### -field ShortArrayCount

The  number of characters in the array.