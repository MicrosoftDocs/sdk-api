---
UID: NS:sspi._SEC_WINNT_AUTH_DATA_PASSWORD
title: SEC_WINNT_AUTH_DATA_PASSWORD (sspi.h)
description: Specifies a serialized password.
helpviewer_keywords: ["PSEC_WINNT_AUTH_DATA_PASSWORD","PSEC_WINNT_AUTH_DATA_PASSWORD structure [Security]","SEC_WINNT_AUTH_DATA_PASSWORD","SEC_WINNT_AUTH_DATA_PASSWORD structure [Security]","security.sec_winnt_auth_data_password","sspi/PSEC_WINNT_AUTH_DATA_PASSWORD","sspi/SEC_WINNT_AUTH_DATA_PASSWORD"]
old-location: security\sec_winnt_auth_data_password.htm
tech.root: security
ms.assetid: f7f3c0e8-be28-4be2-a472-21a39ace04cb
ms.date: 12/05/2018
ms.keywords: PSEC_WINNT_AUTH_DATA_PASSWORD, PSEC_WINNT_AUTH_DATA_PASSWORD structure [Security], SEC_WINNT_AUTH_DATA_PASSWORD, SEC_WINNT_AUTH_DATA_PASSWORD structure [Security], security.sec_winnt_auth_data_password, sspi/PSEC_WINNT_AUTH_DATA_PASSWORD, sspi/SEC_WINNT_AUTH_DATA_PASSWORD
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
req.typenames: SEC_WINNT_AUTH_DATA_PASSWORD, PSEC_WINNT_AUTH_DATA_PASSWORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SEC_WINNT_AUTH_DATA_PASSWORD
 - sspi/_SEC_WINNT_AUTH_DATA_PASSWORD
 - SEC_WINNT_AUTH_DATA_PASSWORD
 - sspi/SEC_WINNT_AUTH_DATA_PASSWORD
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
 - SEC_WINNT_AUTH_DATA_PASSWORD
---

# SEC_WINNT_AUTH_DATA_PASSWORD structure


## -description

Specifies a serialized password.

## -struct-fields

### -field UnicodePassword

A structure that specifies the offset from the beginning of this structure and size, in bytes, of the serialized byte array that represents the password.

## -see-also

<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_byte_vector">SEC_WINNT_AUTH_BYTE_VECTOR</a>