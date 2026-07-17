---
UID: NS:wtsapi32._WTS_SERIALIZED_USER_CREDENTIAL
tech.root: TermServ
title: WTS_SERIALIZED_USER_CREDENTIAL
ms.date: 09/25/2025
targetos: Windows
description: Contains the serialization of a user credential.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: wtsapi32.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows, version 26100
req.target-min-winversvr: 
req.target-type: 
req.typenames: WTS_SERIALIZED_USER_CREDENTIAL, *PWTS_SERIALIZED_USER_CREDENTIAL, WRDS_SERIALIZED_USER_CREDENTIAL, *PWRDS_SERIALIZED_USER_CREDENTIAL
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wtsapi32.dll
api_name:
 - _WTS_SERIALIZED_USER_CREDENTIAL
 - PWTS_SERIALIZED_USER_CREDENTIAL
 - WTS_SERIALIZED_USER_CREDENTIAL
f1_keywords:
 - _WTS_SERIALIZED_USER_CREDENTIAL
 - wtsapi32/_WTS_SERIALIZED_USER_CREDENTIAL
 - PWTS_SERIALIZED_USER_CREDENTIAL
 - wtsapi32/PWTS_SERIALIZED_USER_CREDENTIAL
 - WTS_SERIALIZED_USER_CREDENTIAL
 - wtsapi32/WTS_SERIALIZED_USER_CREDENTIAL
dev_langs:
 - c++
helpviewer_keywords:
 - _WTS_SERIALIZED_USER_CREDENTIAL
---

## -description

Contains the serialization of a user credential.

## -struct-fields

### -field SerializationLength

The size of the array pointed to by `Serialization` in bytes.

### -field Serialization

A pointer to an array of bytes containing serialized credential information. The format of this data is compatible with the [Microsoft Negotiate authentication package](/windows/win32/api/ntsecapi/nf-ntsecapi-lsalookupauthenticationpackage). See *[CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION](/windows/win32/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization)* for more information.


## -remarks

## -see-also
