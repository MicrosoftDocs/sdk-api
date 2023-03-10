---
UID: NS:sspi._SEC_WINNT_AUTH_BYTE_VECTOR
title: SEC_WINNT_AUTH_BYTE_VECTOR (sspi.h)
description: Specifies the byte offset and array length of the data in an authentication structure.
helpviewer_keywords: ["*PSEC_WINNT_AUTH_BYTE_VECTOR","PSEC_WINNT_AUTH_BYTE_VECTOR","PSEC_WINNT_AUTH_BYTE_VECTOR structure pointer [Security]","SEC_WINNT_AUTH_BYTE_VECTOR","SEC_WINNT_AUTH_BYTE_VECTOR structure [Security]","security.sec_winnt_auth_byte_vector","sspi/PSEC_WINNT_AUTH_BYTE_VECTOR","sspi/SEC_WINNT_AUTH_BYTE_VECTOR"]
old-location: security\sec_winnt_auth_byte_vector.htm
tech.root: security
ms.assetid: ee511497-2b70-4c51-bcc2-7585143b4f43
ms.date: 12/05/2018
ms.keywords: '*PSEC_WINNT_AUTH_BYTE_VECTOR, PSEC_WINNT_AUTH_BYTE_VECTOR, PSEC_WINNT_AUTH_BYTE_VECTOR structure pointer [Security], SEC_WINNT_AUTH_BYTE_VECTOR, SEC_WINNT_AUTH_BYTE_VECTOR structure [Security], security.sec_winnt_auth_byte_vector, sspi/PSEC_WINNT_AUTH_BYTE_VECTOR, sspi/SEC_WINNT_AUTH_BYTE_VECTOR'
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
req.typenames: SEC_WINNT_AUTH_BYTE_VECTOR, *PSEC_WINNT_AUTH_BYTE_VECTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SEC_WINNT_AUTH_BYTE_VECTOR
 - sspi/_SEC_WINNT_AUTH_BYTE_VECTOR
 - PSEC_WINNT_AUTH_BYTE_VECTOR
 - sspi/PSEC_WINNT_AUTH_BYTE_VECTOR
 - SEC_WINNT_AUTH_BYTE_VECTOR
 - sspi/SEC_WINNT_AUTH_BYTE_VECTOR
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
 - SEC_WINNT_AUTH_BYTE_VECTOR
---

# SEC_WINNT_AUTH_BYTE_VECTOR structure


## -description

Specifies the byte  offset and array length of the data in an authentication structure.

## -struct-fields

### -field ByteArrayOffset

The number of bytes from the beginning of a structure in memory to the beginning of the data.

### -field ByteArrayLength

The number of bytes in the data array of a structure.

## -see-also

<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_certificate_data">SEC_WINNT_AUTH_CERTIFICATE_DATA</a>



<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_data">SEC_WINNT_AUTH_DATA</a>



<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_data_password">SEC_WINNT_AUTH_DATA_PASSWORD</a>



<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_packed_credentials_ex">SEC_WINNT_AUTH_PACKED_CREDENTIALS_EX</a>