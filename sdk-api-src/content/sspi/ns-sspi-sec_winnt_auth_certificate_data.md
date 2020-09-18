---
UID: NS:sspi._SEC_WINNT_AUTH_CERTIFICATE_DATA
title: SEC_WINNT_AUTH_CERTIFICATE_DATA (sspi.h)
description: Specifies serialized certificate information.
helpviewer_keywords: ["*PSEC_WINNT_AUTH_CERTIFICATE_DATA","PSEC_WINNT_AUTH_CERTIFICATE_DATA","PSEC_WINNT_AUTH_CERTIFICATE_DATA structure pointer [Security]","SEC_WINNT_AUTH_CERTIFICATE_DATA","SEC_WINNT_AUTH_CERTIFICATE_DATA structure [Security]","security.sec_winnt_auth_certificate_data","sspi/PSEC_WINNT_AUTH_CERTIFICATE_DATA","sspi/SEC_WINNT_AUTH_CERTIFICATE_DATA"]
old-location: security\sec_winnt_auth_certificate_data.htm
tech.root: security
ms.assetid: 08dc5062-2925-4ec2-aef3-c7ff1cba9544
ms.date: 12/05/2018
ms.keywords: '*PSEC_WINNT_AUTH_CERTIFICATE_DATA, PSEC_WINNT_AUTH_CERTIFICATE_DATA, PSEC_WINNT_AUTH_CERTIFICATE_DATA structure pointer [Security], SEC_WINNT_AUTH_CERTIFICATE_DATA, SEC_WINNT_AUTH_CERTIFICATE_DATA structure [Security], security.sec_winnt_auth_certificate_data, sspi/PSEC_WINNT_AUTH_CERTIFICATE_DATA, sspi/SEC_WINNT_AUTH_CERTIFICATE_DATA'
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
req.typenames: SEC_WINNT_AUTH_CERTIFICATE_DATA, *PSEC_WINNT_AUTH_CERTIFICATE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SEC_WINNT_AUTH_CERTIFICATE_DATA
 - sspi/_SEC_WINNT_AUTH_CERTIFICATE_DATA
 - PSEC_WINNT_AUTH_CERTIFICATE_DATA
 - sspi/PSEC_WINNT_AUTH_CERTIFICATE_DATA
 - SEC_WINNT_AUTH_CERTIFICATE_DATA
 - sspi/SEC_WINNT_AUTH_CERTIFICATE_DATA
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
 - SEC_WINNT_AUTH_CERTIFICATE_DATA
---

# SEC_WINNT_AUTH_CERTIFICATE_DATA structure


## -description

Specifies serialized certificate information.

## -struct-fields

### -field cbHeaderLength

The size, in bytes,  of the structure header.

### -field cbStructureLength

The size, in bytes, of the certificate information.

### -field Certificate

A structure that specifies the offset from the beginning of this structure and the size, in bytes, of the certificate data.

## -see-also

<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_byte_vector">SEC_WINNT_AUTH_BYTE_VECTOR</a>